# Toolchange Tuning

Parameters and dock path tuned to reduce toolchange time while maintaining reliability. Changes were made to both `printer.cfg` (motion limits) and the StealthChanger macro configs.

## Tuned Parameters

| Parameter | File | Default | Tuned | Notes |
|---|---|---|---|---|
| `max_velocity` | `printer.cfg` | 300 mm/s | **500 mm/s** | Caps fast travel during change |
| `max_accel` | `printer.cfg` | 6700 mm/s² | 6700 mm/s² | Unchanged — resonance-tested limit |
| `max_z_velocity` | `printer.cfg` | 100 mm/s | **200 mm/s** | Faster Z during dock approach |
| `max_z_accel` | `printer.cfg` | 1000 mm/s² | **1500 mm/s²** | Faster Z ramp-up |
| `square_corner_velocity` | `printer.cfg` | 5.0 mm/s | 5.0 mm/s | Unchanged |
| `params_safe_y` | `macros.cfg` | 120 mm | **80 mm** | Y clearance before/after dock |
| `params_close_y` | `macros.cfg` | 15 mm | **10 mm** | Y position for dock approach |
| `params_fast_speed` | `macros.cfg` | 30000 mm/min | 30000 mm/min | Unchanged — already capped by `max_velocity` |
| `params_path_speed` | `macros.cfg` | 900 mm/min (15 mm/s) | **6000 mm/min (100 mm/s)** | Speed through dock path waypoints |
| `params_sc_path` | `Toolhead_T*.cfg` | 6 waypoints | **4 waypoints** | Removed initial high-Z approach arc (see below) |

## Dock Path Detail (`params_sc_path`)

All tools use `params_type: 'sc'`. The original 6-waypoint arc was trimmed by removing the high-Z ramp-in — the toolhead now enters the dock directly at Z=0.

**Before (6 waypoints):**
```python
[{'y':9.5, 'z':7}, {'y':9.5, 'z':2}, {'y':5.5, 'z':0},
 {'z':0, 'y':0, 'f':0.5}, {'z':-11.5, 'y':0}, {'z':-11.5, 'y':10}]
```

**After (4 waypoints):**
```python
[{'y':5.5, 'z':0},
 {'z':0, 'y':0, 'f':0.5}, {'z':-11.5, 'y':0}, {'z':-11.5, 'y':10}]
```
