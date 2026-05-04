# AutoTurretRange

A Unity project implementing an auto-targeting turret shooting range.

## Features

- **Target Drone** moves in a circular path around the turret
- **Yaw rotation** — turret head tracks the drone horizontally
- **Pitch rotation** — turret barrel aims vertically with angle limits
- **Aim detection** — checks if the muzzle is within a threshold angle of the target
- **Projectile system** — fires when aimed, auto-destroys after a set lifetime

## Scripts

| Script | Description |
|---|---|
| `TargetDrone.cs` | Rotates the rail pivot to move the drone in a circle |
| `TurretYaw.cs` | Rotates YawPivot toward the target on the Y axis |
| `TurretPitch.cs` | Rotates PitchPivot toward the target on the X axis |
| `TurretShooter.cs` | Detects aim and fires projectiles from MuzzlePoint |
| `Projectile.cs` | Moves forward and self-destructs after lifetime |

## Scene Hierarchy

```
Turret
├── TurretFloor
├── TurretHead
├── TurretBarrel
│   └── MuzzlePoint
└── YawPivot
    └── PitchPivot

TargetRailPivot
└── TargetDrone
```
