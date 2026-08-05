# Toolchange Tuning

Parameters and dock path tuned to reduce toolchange time while maintaining reliability. Changes were made to both `printer.cfg` (motion limits) and the StealthChanger macro configs. Overall this reduced the toolchange time from 11.57s to 4.8s, on a standard 25V motor setup. 

## Tuned Parameters

| Parameter | File | Default | Tuned | Notes |
|---|---|---|---|---|
| `max_velocity` | `printer.cfg` | 300 mm/s | **500 mm/s** | Speed up fast travel mostly when approaching or traveling between docks |
| `max_z_velocity` | `printer.cfg` | 100 mm/s | **200 mm/s** | Faster Z going up and down from the docks |
| `max_z_accel` | `printer.cfg` | 1000 mm/s² | **1500 mm/s²** | Faster Z acceleration |
| `params_safe_y` | `macros.cfg` | 120 mm | **80 mm** | Y clearance closer to the dock |
| `params_close_y` | `macros.cfg` | 15 mm | **10 mm** | Keeps shuttle closers to tools between dropoff and pickup |
| `params_path_speed` | `macros.cfg` | 900 mm/min (15 mm/s) | **6000 mm/min (100 mm/s)** | Much faster speed during the pickup and and drop off |
| `params_sc_path` | `Toolhead_T*.cfg` | 6 waypoints | **4 waypoints** | Removed ramped approach for a straight line |

## Dock Path Detail (`params_sc_path`)

All tools use `params_type: 'sc'`. The original 6-waypoint path had an angled ramp in, siultaneous Y/Z move, when docking and undocking. The shuttle now approaches the dock directly in a pure linear Y axis movement, then pure Z move to engage/disengage to toolhead.

**Before (6 waypoints):**
```python
[{'y':9.5, 'z':7}, {'y':9.5, 'z':2}, {'y':5.5, 'z':0}, {'z':0, 'y':0, 'f':0.5}, {'z':-11.5, 'y':0}, {'z':-11.5, 'y':10}]
```

**After (4 waypoints):**
```python
[{'y':5.5, 'z':0}, {'z':0, 'y':0, 'f':0.5}, {'z':-11.5, 'y':0}, {'z':-11.5, 'y':10}]
```
