<p align="center">
  <img src="https://github.com/Levy-Y/Network-Builder/blob/main/assets/logo.png?raw=true" alt="Logo" width="35%"/>
</p>

# Network-Builder

[![Made with Python](https://img.shields.io/badge/Python->=3.8-blue?logo=python&logoColor=white)](https://python.org "Go to Python homepage") ![maintained - no](https://img.shields.io/badge/maintained-no-red) ![Upload to PyPi](https://github.com/Levy-Y/Network-Builder/actions/workflows/publish-to-pypi.yml/badge.svg)

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
python -m Network_Builder --config_file <file_path>
```

## Example config yml example:
```yaml
version: '1.0'

devices:
  - name: 'device1'
    type: 'cisco_ios'
    ip: '192.168.1.210'
    port: '22'
    username: 'admin'
    password: 'password'
  - name: 'device2'
    type: 'cisco_ios'
    ip: '192.168.1.211'
    port: '22'
    username: 'admin'
    password: 'password'

tasks:
  - name: 'task1 name'
    description: 'This is task 1'
    device: 'device1'
    commands:
      - 'show version'
      - 'show ip interface brief'
  - name: 'task2 name'
    description: 'This is task 2'
    device: 'device2'
    commands:
      - 'show version'
      - 'show ip interface brief'
```

## Contributing

We welcome contributions from the community. Before submitting a pull request, please ensure that:

- Your feature or bug fix is covered by tests.
- Your code adheres to the existing code style.
- You have added or updated documentation as necessary.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
