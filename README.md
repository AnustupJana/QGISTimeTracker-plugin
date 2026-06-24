# QGIS Time Tracker Plugin

![Diagram of the System](https://github.com/AnustupJana/QGIS-Time-Tracker/blob/main/icon.png?raw=true)

## Overview

The **QGIS Time Tracker** plugin helps GIS professionals, freelancers, researchers, and organizations monitor real working time inside QGIS. Unlike simple application runtime trackers, it measures active working time, idle time, editing activity, tool usage, and session productivity.

The plugin provides a live floating timer widget, activity monitoring, edit statistics, session summaries, and report exports in CSV, Excel, and PDF formats. Daily, weekly, and monthly productivity summaries allow users to analyze project effort and work patterns accurately.

## Features

* **Real Active Time Tracking**: Tracks actual working time based on user activity.
* **Idle Time Detection**: Automatically pauses active tracking after user inactivity.
* **Session Monitoring**: Records session duration, active time, idle time, and productivity.
* **Live Floating Timer**: Displays current session statistics directly inside QGIS.
* **Tool Usage Statistics**: Monitors map navigation, layer changes, layer additions, and other user activities.
* **Edit Activity Monitoring**: Tracks feature creation, deletion, geometry modifications, attribute edits, and editing sessions.
* **Dashboard Analytics**: Displays detailed productivity summaries and statistics.
* **Daily, Weekly, and Monthly Totals**: Calculates cumulative active working time across sessions.
* **Report Exporting**:

  * CSV Reports
  * Excel Reports
  * PDF Reports
* **Lightweight Database Storage**: Uses SQLite for efficient local data storage.

## Installation

### 1. From QGIS Plugin Repository

* Open QGIS.

* Navigate to:

  ```
  Plugins > Manage and Install Plugins
  ```

* Search for:

  ```
  QGIS Time Tracker
  ```

* Click:

  ```
  Install Plugin
  ```

### 2. From ZIP File

* Download the latest ZIP release from GitHub.

* Open QGIS.

* Go to:

  ```
  Plugins > Manage and Install Plugins > Install from ZIP
  ```

* Select the downloaded ZIP file.

* Click:

  ```
  Install Plugin
  ```

### 3. Manual Installation

* Download or clone the repository.
* Copy the plugin folder into the QGIS plugins directory.

#### Windows

```text
C:\Users\<Username>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\
```

#### Linux

```text
~/.local/share/QGIS/QGIS3/profiles/default/python/plugins/
```

#### macOS

```text
~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins/
```

* Restart QGIS.

## Usage

### Start Tracking

1. Open QGIS.
2. Enable the plugin.
3. The floating timer widget automatically appears.
4. Tracking begins automatically when activity is detected.

### Monitor Productivity

The timer widget displays:

* Session Time
* Active Time
* Idle Time
* Productivity Percentage

### View Dashboard

Click:

```text
Plugins > QGIS Time Tracker > Dashboard
```

The dashboard displays:

* Current Session Summary
* Today's Total Working Time
* Weekly Total Working Time
* Monthly Total Working Time
* Tool Usage Statistics
* Edit Statistics

### Export Reports

Use:

```text
Export ▼
```

and select:

* CSV Report
* Excel Report
* PDF Report

Reports are saved to your selected location.

## Activity Detection

The plugin automatically detects:

### General Activities

* Layer Added
* Layer Removed
* Layer Changed
* Map Navigation
* Map Zoom
* Map Pan

### Editing Activities

* Editing Started
* Editing Stopped
* Feature Added
* Feature Deleted
* Geometry Modified
* Attribute Changed

## Requirements

* **QGIS Version**: 3.0 or higher
* **Python Version**: Included with QGIS
* **Libraries Used**:

  * sqlite3
  * openpyxl
  * reportlab

## Troubleshooting

### Timer Not Updating

* Verify the plugin is enabled.
* Check that user activity is occurring inside QGIS.
* Restart QGIS if necessary.

### Dashboard Statistics Empty

* Perform some map navigation or editing operations.
* Refresh the dashboard.

### Export Errors

* Verify that the destination folder is writable.
* Ensure required Python dependencies are installed.

### Plugin Not Visible

* Confirm the plugin folder is correctly installed.
* Restart QGIS.
* Verify all plugin files exist.

### Debugging

Open:

```text
Plugins > Python Console
```

and check for error messages.

## Project Structure

```text
QGISTimeTracker/
│
├── core/
│   ├── database.py
│   ├── tracker.py
│   ├── idle_detector.py
│   ├── activity_monitor.py
│   └── edit_monitor.py
│
├── gui/
│   ├── timer_widget.py
│   └── dashboard_dialog.py
│
├── exports/
│   ├── export_csv.py
│   ├── export_excel.py
│   └── export_pdf.py
│
├── icon.png
├── metadata.txt
├── resources.py
├── __init__.py
└── qgis_time_tracker.py
```

## Contributing

Contributions are welcome.

* Fork the repository.
* Create a feature branch.
* Submit a pull request.
* Report bugs and feature requests through GitHub Issues.

## License

This plugin is licensed under the **GNU General Public License v2.0 or later (GPL-2.0+)**.

See the LICENSE file for complete license information.

## Author

**Anustup Jana**

Email: [anustupjana21@gmail.com](mailto:anustupjana21@gmail.com)

Copyright © 2026 Anustup Jana
