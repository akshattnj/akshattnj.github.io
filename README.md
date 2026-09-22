# Website Architecture & Directory Structure

This document provides a comprehensive functional overview of all folders, subfolders, and files within this personal portfolio and research website.

---

## 1. Overview & Technology Stack

The website is hosted on **GitHub Pages** and generated using **Jekyll**, a static site generator.

- **Theme**: [`yousinix/portfolYOU`](https://github.com/yousinix/portfolYOU) via `jekyll-remote-theme`.
- **Templating**: Liquid templating engine combined with Markdown and HTML.
- **Data Management**: YAML files located in `_data/` feed dynamic elements such as skills, career timeline, and social profiles.
- **Content Collections**:
  - `_posts/`: Blog articles detailing research interests and academic writings.
  - `_projects/`: Portfolio showcase of hardware, firmware, PCB design, robotics, and AI projects.
- **Routing & Pages**: Custom pages configured in `pages/` defining navigation endpoints (`/`, `/about/`, `/projects/`, `/blog/`, `/blog/tags`).

---

## 2. Directory Tree

```plaintext
akshattnj.github.io/
├── _config.yml                                                        # Main Jekyll configuration
├── Gemfile                                                            # Ruby dependencies for local builds
├── 11459052.pdf                                                       # MSc Dissertation academic paper
├── README.md                                                          # Project documentation (this file)
│
├── _data/                                                             # Structured YAML data sources
│   ├── other-skills.yml                                               # Secondary technical & soft skills
│   ├── programming-skills.yml                                         # Core engineering & programming skills
│   ├── social-media.yml                                               # Social profile URLs, icons & colors
│   └── timeline.yml                                                   # Work experience & education history
│
├── _posts/                                                            # Research blog articles (Markdown)
│   ├── 2021-04-17-haptics-remote-sensing.md                           # Haptic feedback systems in remote sensing
│   ├── 2021-09-25-auto-correction-grip-strength.md                   # Adaptive grip strength in prosthetics
│   ├── 2022-05-09-neural-interfaces.md                                # Non-invasive neural interfaces
│   ├── 2023-01-01-SWARM-based-nano-technologies.md                    # Nanoscale swarm robotics
│   └── 2024-02-09-using-generative-ai-forbetter-HMI.md                # Generative AI for industrial HMIs
│
├── _projects/                                                         # Project portfolio items (Markdown)
│   ├── dronecan_bms_integration_solution.md                           # DroneCAN BMS integration for UAVs
│   ├── esp32_i2c_temperature_sensor_integration.md                   # ESP32 AHT10/AHT21 I2C & CAN integration
│   ├── firmware_development_for_esp-idf_with_oled_displays.md         # ESP-IDF SSD1306 OLED driver & animations
│   ├── firmware_guide_for_quectel_modem_configuration.md             # Quectel 4G LTE UART & GPS NMEA config
│   ├── Mars Rover Manipal.md                                          # Mars Rover electrical & PCB design
│   ├── pcb_design_for_short_circuit_protection_in_uavs.md             # N-MOSFET short-circuit & polarity protection
│   ├── twai_communication_handler_for_esp32_automotive_applications.md# Car auto-path navigation using NEAT RL
│   └── uomDiss.md                                                     # 7-DOF autonomous wound cleaning robot pipeline
│
├── pages/                                                             # Site views and routing templates
│   ├── 404.html                                                       # Custom Page Not Found handler
│   ├── about.md                                                       # About Me page (bio, skills, timeline)
│   ├── index.md                                                       # Website homepage / landing view
│   ├── projects.html                                                  # Projects portfolio page
│   ├── resint.html                                                    # Research interests / blog page
│   ├── search.json                                                    # Dynamic JSON post search index
│   ├── secret.html                                                    # Standalone password-protected private portal
│   └── tags.html                                                      # Blog tag filtering page
│
└── [Media & Asset Files]                                              # Static images & graphics in root
    ├── 1.png                                                          # Preview: MSc Dissertation project
    ├── can2usb.webp                                                   # Media: CAN-to-USB hardware asset
    ├── dronecan.png                                                   # Preview: DroneCAN BMS project
    ├── i2ctemp.webp                                                   # Preview: ESP32 I2C sensor project
    ├── marsrover.jpg                                                  # Preview: Mars Rover Manipal project
    ├── NEAT.webp                                                      # Preview: NEAT RL car path project
    ├── nfc.webp                                                       # Media: NFC module asset
    ├── nmos.webp                                                      # Preview: N-MOSFET protection PCB project
    ├── oled.webp                                                      # Preview: OLED display firmware project
    ├── pcb.png                                                        # Media: PCB design graphic
    ├── profile.JPG                                                    # Author avatar / profile photo
    ├── quectel.jpg                                                    # Preview: Quectel modem project
    └── twai.png                                                       # Media: ESP32 TWAI CAN bus graphic
```

---

## 3. Detailed Component Breakdown

### 3.1 Root Configuration & System Files

| File / Folder | Type | Function & Purpose |
| :--- | :--- | :--- |
| **`_config.yml`** | YAML Config | Global Jekyll configuration file. Configures website title, author bio, social links, remote theme (`yousinix/portfolYOU`), plugin list (`jemoji`), permalink schemas (`/blog/:title`, `/projects/:name`), collection defaults, and build exclusion rules. |
| **`Gemfile`** | Ruby Bundler | Defines Ruby gem dependencies needed for local Jekyll site building and development (e.g., `github-pages`, `wdm`, `faraday-retry`). |
| **`11459052.pdf`** | Document (PDF) | Academic dissertation document authored by Akshat Taneja for the University of Manchester MSc in Robotics (*"Reproducible Wound Sensing and Trajectory Planning for an Autonomous Wound Care Robot"*, Student ID: 11459052). |

---

### 3.2 `_data/` Directory (Site Data & Content Collections)

The `_data` folder contains structured YAML files consumed by Jekyll's Liquid templates to dynamically render personal background, skills, and links without editing HTML templates directly.

| File | Function & Content |
| :--- | :--- |
| **`_data/programming-skills.yml`** | Stores technical engineering skills, proficiency percentages, and badge color codes (e.g., Electronics Design & Prototyping, C/C++, ROS, CAD SolidWorks, Python, Machine Learning/CV, PCB Design, Linux). |
| **`_data/other-skills.yml`** | Stores professional competencies and domain knowledge (e.g., Project Management, IoT Systems Development, PLC Ladder Logic, Technical Documentation, Research & Data Analysis, Embedded Systems, AWS Cloud Fundamentals). |
| **`_data/timeline.yml`** | Contains structured career and academic timeline entries (M.Sc. Robotics at UoM, Haveli UAVs, Micromatic Grinding Technologies, MovioMobility, Euphotic Labs, B.E. Mechatronics at MIT Manipal). |
| **`_data/social-media.yml`** | Maps supported social platforms (GitHub, LinkedIn, Email, Facebook, etc.) to FontAwesome icons, brand colors, and URL schemas. |

---

### 3.3 `pages/` Directory (Navigation & Routing)

The `pages` folder defines the main standalone routes and views accessible from the navigation bar.

| File | URL Route | Function & Content |
| :--- | :--- | :--- |
| **`pages/index.md`** | `/` | Home landing page. Includes `landing.html` from the portfolYOU theme to present the title, author avatar, tagline, and quick navigation. |
| **`pages/about.md`** | `/about/` | "About Me" page. Displays personal biography, resume links, GitHub/LinkedIn buttons, and dynamically renders skill bars from `_data/*-skills.yml` and timeline items from `_data/timeline.yml`. |
| **`pages/projects.html`** | `/projects/` | Projects catalog page. Renders all project cards defined in the `_projects/` collection, along with configured remote GitHub repositories (`remote_projects`). |
| **`pages/resint.html`** | `/blog/` | "Research Interests" / Blog page. Incorporates search filtering (`blog/search.html`) and lists all research articles from `_posts/`. |
| **`pages/tags.html`** | `/blog/tags` | Tag index page. Renders categorized lists of posts grouped by tag keywords. |
| **`pages/search.json`** | `/search.json` | Dynamic JSON endpoint generated via Liquid templating. Indexes post titles, categories, tags, URLs, and dates for client-side search autocomplete. |
| **`pages/secret.html`** | `/secret/` | Hidden password-protected private portal (`0920`). Excluded from navigation and search indexing (`noindex, nofollow`). Contains a secure dashboard and local scratchpad. |
| **`pages/404.html`** | `/404.html` | Custom error page displayed when a visitor navigates to an invalid URL. |

---

### 3.4 `_posts/` Directory (Research Articles & Blog)

Contains blog articles formatted in Markdown with YAML frontmatter. These represent academic and technical research interests.

| File | Published Date | Subject Matter |
| :--- | :--- | :--- |
| **`2021-04-17-haptics-remote-sensing.md`** | 2021-04-17 | **Haptic Feedback Systems for Remote Sensing**: Explores force-feedback mechanisms combined with LiDAR and tactile sensor arrays for remote robotics in hazardous environments. |
| **`2021-09-25-auto-correction-grip-strength.md`** | 2021-09-25 | **Adaptive Grip Strength in Prosthetics**: Researches pressure sensor integration and ML algorithms for real-time grip adjustment in robotic hands. |
| **`2022-05-09-neural-interfaces.md`** | 2022-05-09 | **Neural Interfaces (EEG)**: Studies non-invasive Brain-Computer Interfaces (BCI) translating EEG brainwave patterns into robotic control signals. |
| **`2023-01-01-SWARM-based-nano-technologies.md`** | 2023-01-01 | **SWARM Nanorobotics**: Analyzes collaborative nanoscale robotic swarms for targeted biomedical drug delivery and micro-industrial maintenance. |
| **`2024-02-09-using-generative-ai-forbetter-HMI.md`** | 2024-02-09 | **Generative AI for HMIs**: Investigates adaptive human-machine interfaces that dynamically adjust control dashboards based on operator habits. |

---

### 3.5 `_projects/` Directory (Portfolio Projects Collection)

Contains detailed project entries showcased under `/projects/`. Each markdown file includes metadata such as project title, tools used, thumbnail image, project description, key contributions, and external GitHub/team links.

| File | Project Title | Tools / Technologies | Summary |
| :--- | :--- | :--- | :--- |
| **`Mars Rover Manipal.md`** | Mars Rover Manipal | SolidWorks Electrical, Altium, KiCad, PCB Design, Soldering | Power distribution architecture, custom motor-driver PCBs, wiring optimization, and harsh-environment validation for an international rover competition. |
| **`dronecan_bms_integration_solution.md`** | DroneCAN BMS Integration Solution | DroneCAN, BMS, Embedded Systems | Battery Management System using DroneCAN protocol for modular UAV telemetry and power management. |
| **`esp32_i2c_temperature_sensor_integration.md`** | ESP32 I2C Temperature Sensor Integration | ESP32, I2C (AHT10/21), CAN, C/C++ | Firmware reading ambient temperature data over I2C, rendering to OLED displays, and broadcasting via CAN. |
| **`firmware_development_for_esp-idf_with_oled_displays.md`** | ESP-IDF OLED Display Firmware | ESP32, SSD1306, ESP-IDF | Low-level C firmware utilizing ESP-IDF to drive monochrome SSD1306 OLED displays with custom UI animations and text routines. |
| **`firmware_guide_for_quectel_modem_configuration.md`** | Quectel 4G LTE Modem UART Firmware | UART, LTE Modem, GPS NMEA, IoT | ESP-IDF UART-based firmware establishing cellular connectivity and parsing GPS NMEA streams for IoT telematics. |
| **`pcb_design_for_short_circuit_protection_in_uavs.md`** | UAV Short Circuit Protection PCB | PCB Design, N-MOSFETs, Protection Circuits | Hardware protection board utilizing N-channel MOSFETs for reverse polarity and over-current protection in drone electronics. |
| **`twai_communication_handler_for_esp32_automotive_applications.md`** | Car Auto Path RL (NEAT) | Reinforcement Learning, NEAT, PyTorch / Python | Autonomous racecar navigation using the NEAT (NeuroEvolution of Augmenting Topologies) genetic algorithm for track navigation. |
| **`uomDiss.md`** | UoM MSc Dissertation: 7-DOF Wound Cleaning Robot | ROS2, Gazebo, Inverse Kinematics, Python, OpenCV | Reproducible robotic pipeline integrating ROS2, inverse kinematics, computer vision, and Gazebo simulation for autonomous wound debridement. |

---

### 3.6 Media & Image Assets (Root Directory)

Static media files referenced throughout the website's pages, projects, and author profile:

| Asset Name | Format | Role & Usage |
| :--- | :--- | :--- |
| **`profile.JPG`** | JPEG | Author portrait photo displayed on the homepage and about page (`site.author.image`). |
| **`1.png`** | PNG | Project thumbnail for the 7-DOF Wound Cleaning Robot dissertation project. |
| **`marsrover.jpg`** | JPEG | Project thumbnail for the Mars Rover Manipal project. |
| **`dronecan.png`** | PNG | Project thumbnail for the DroneCAN BMS Integration project. |
| **`i2ctemp.webp`** | WebP | Project thumbnail for the ESP32 I2C Temperature Sensor project. |
| **`oled.webp`** | WebP | Project thumbnail for the ESP-IDF OLED Firmware project. |
| **`quectel.jpg`** | JPEG | Project thumbnail for the Quectel Modem Configuration project. |
| **`nmos.webp`** | WebP | Project thumbnail for the UAV Short Circuit Protection PCB project. |
| **`NEAT.webp`** | WebP | Project thumbnail for the NEAT Reinforcement Learning Car project. |
| **`can2usb.webp`** | WebP | Hardware asset graphic illustrating CAN-to-USB interface hardware. |
| **`nfc.webp`** | WebP | Hardware asset graphic illustrating Near Field Communication hardware. |
| **`pcb.png`** | PNG | Schematic/layout graphic representing PCB development. |
| **`twai.png`** | PNG | Hardware graphic representing ESP32 TWAI (Two-Wire Automotive Interface / CAN). |

---

## 4. Theme & Layout Architecture

The site inherits layouts, stylesheets, and scripts from the remote theme **`yousinix/portfolYOU`**:
- **Layouts (`_layouts/`)**:
  - `default`: Base layout injecting HTML head, navigation bar, favicon, scripts, and footer.
  - `page`: Standard container layout for content pages (`/about/`, `/blog/tags`).
  - `post`: Formatted article layout with metadata headers and tag chips.
- **Includes (`_includes/`)**:
  - `landing.html`: Header banner with avatar and social icon links.
  - `about/skills.html` & `about/timeline.html`: Interactive skill bars and chronological experience markers.
  - `projects/index.html`: Responsive card grid showing local collection items and remote GitHub repository cards.
  - `blog/index.html` & `blog/search.html`: Filterable blog post listing with live search.
