# Head Tracking Missile Launcher

## Circuit Connections

```
                ┌──────────────────────┐
                │    ARDUINO NANO      │
                │                      │
                │ 5V  ─────────────┐   │
                │ GND ──────────┐  │   │
                │               │  │   │
                │ D9  ───────┐  │  │   │
                │ D10 ─────┐ │  │  │   │
                │ D11 ───┐ │ │  │  │   │
                └────────│─│─│──│──│───┘
                         │ │ │  │  │
         ┌───────────────┘ │ │  │  │
         │                 │ │  │  │
   ┌───────────┐     ┌───────────┐ │
   │ SERVO 1   │     │ SERVO 2   │ │
   │ Signal → D9     │ Signal→D10│ │
   │ VCC    → 5V     │ VCC → 5V  │ │
   │ GND    → GND    │ GND → GND │ │
   └───────────┘     └───────────┘ │
                                   │
                             ┌──────────┐
                             │ LASER    │
                             │ S → D11  │
                             │ - → GND  │
                             │ + → 5V   │
                             └──────────┘
```

## Pin Summary

| Component | Arduino Pin |
|---|---|
| Servo 1 Signal | D9 |
| Servo 2 Signal | D10 |
| Laser Signal | D11 |
| All VCC | 5V |
| All GND | GND |

## Important Notes

* Servo motors need a good power supply.
* If servos jitter, use an external 5V supply.
* Connect external supply GND with Arduino GND.  
* Laser module should be 5V compatible.

## Servo Wire Colors

Usually:

* **Brown/Black** → GND
* **Red** → 5V
* **Orange/Yellow** → Signal  
