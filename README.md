# Dragon Boat Regatta Analytics (Nottingham NWSC)

A lightweight, client-side web application designed to analyze and compare dragon boat race telemetry recorded via GPS watches (e.g., Garmin) at the National Water Sports Centre in Holme Pierrepont, Nottingham.

The dashboard automatically isolates the competitive race window from pre-race staging/marshaling and normalizes tracks along the course vector to allow direct, side-by-side performance analysis.

---

## Key Features

- **Race Window Auto-Detection**:
  - Automatically identifies race starts and finishes using vector heading (NE to SW lake orientation) and acceleration thresholds.
  - Excludes pre-race warm-up, holding patterns, and post-race cool-downs.
- **Dynamic Distance Switching (200m / 500m)**:
  - **500m Mode**: Generates 100m split times, 500m split paces, and models 3-phase endurance cadence profiles (start, cruise, finish kick).
  - **200m Mode**: Generates 50m split times, adjusts charts to a 0–200m range, and adapts cadence estimation to sprint mechanics.
- **Head-to-Head Comparative Charts**:
  - **Boat Speed (km/h)**: Overlaid speed profiles across distance.
  - **Heart Rate (BPM)**: Exertion and cardiac response throughout the race.
  - **Pace (s/split)**: Visual representation of speed retention and lactic fade.
  - **Cadence Estimation (SPM)**: Modeled stroke frequency based on boat surge mechanics and velocity.
- **Interactive Course Map**:
  - Overlaid GPS polylines on a dark canvas map with designated start and finish gate markers.
- **Layer & Race Toggles**:
  - Show/hide individual races to isolate head-to-head matchups (e.g., Heat vs. Semi-Final vs. Minor Final).
- **100% Client-Side**:
  - Runs offline in any standard browser. No web servers, APIs, or database installations required.

---

## File Structure

```text
├── index.html   # Standalone HTML/JS/CSS dashboard
└── README.md    # Documentation