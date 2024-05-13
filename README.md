<p align="center">
  <img src="https://github.com/Levy-Y/Network-Builder/blob/main/assets/logo.png?raw=true" alt="Logo" width="35%"/>
</p>

# Network-Builder

[![Made with Python](https://img.shields.io/badge/Python->=3.8-blue?logo=python&logoColor=white)](https://python.org "Go to Python homepage") ![maintained - yes](https://img.shields.io/badge/maintained-yes-blue) ![Upload to PyPi](https://github.com/Levy-Y/Network-Builder/actions/workflows/publish-to-pypi.yml/badge.svg)

## Installation

### Using pip

```bash
pip install Network_Builder
```

### Manually
1. Download the latest release from the [releases tab](https://github.com/Levy-Y/Network-Builder/releases).
2. Install the wheel file using pip:

```bash
pip install /path/to/downloaded/wheel/file.whl
```

## Usage
```bash
python -m Network_Builder --tasks_file <file_path> --devices_file <file_path>
```

## Device config json example:
```json
{
  "devices": [
    {
      "name": "Device_Name_1",
      "ip": "192.168.1.1",
      "port": 22,
      "type": "cisco_ios"
    },
    {
      "name": "Device_Name_2",
      "ip": "10.10.0.23",
      "port": 22,
      "type": "cisco_ios"
    }
  ]
}
```

## Task list json example:
``` json
{
    "tasks": [
        {
            "taskname": "Task Name 1",
            "taskdescription": "Task without argument",
            "target": "Device_Name_1",
            "command": "command_of_your_choice",
            "arguments": []
        },
        {
            "taskname": "Task Name 2",
            "taskdescription": "Task with argument",
            "target": "Device_Name_2",
            "command": "command_of_your_choice_with_argument",
            "arguments": [
                "argument_1",
                "argument_2"
            ]
        }
    ]
}
```


## Contributing

We welcome contributions from the community. Before submitting a pull request, please ensure that:

- Your feature or bug fix is covered by tests.
- Your code adheres to the existing code style.
- You have added or updated documentation as necessary.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
