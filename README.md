# library-eda-3d-models

This repository contains a library of 3D models specifically designed for use with Electronic Design Automation (EDA) packages. While it includes specific electromechanical components utilized in guitar pedal effects, it also encompasses a broad range of passive and active components used in our designs.

## Description

The 3D Models Library serves as a comprehensive source for every 3D model used in the PCB and general design of our effects. Embracing our "everything is open-source" philosophy, this library aims to provide a reliable and legally unambiguous resource, sidestepping the licensing pitfalls often encountered with randomly sourced models. Each component is designed based on the manufacturer's datasheet, and we provide .step files along with the FreeCAD source files for maximum accessibility and adaptability.

## Repository Structure

The repository adopts a family/category/component approach to minimize the depth of the directory structure while still ensuring ease of browsing and searching. Expect a structure similar to:

```
library-eda-3d-models
├── passives
│   ├── capacitors
│   │   ├── smd-capacitor-mlcc-0603
│   │   │   ├── smd-capacitor-mlcc-0603.FCStd
│   │   │   └── smd-capacitor-mlcc-0603.step
│   │   └── smd-capacitor-mlcc-0805
│   │       ├── smd-capacitor-mlcc-0805.FCStd
│   │       └── smd-capacitor-mlcc-0805.step
│   ├── resistors
│   │   ├── smd-resistor-film-0603
│   │   │   ├── smd-resistor-film-0603.FCStd
│   │   │   └── smd-resistor-film-0603.step
│   │   └── smd-resistor-film-0805
│   │       ├── smd-resistor-film-0805.FCStd
│   │       └── smd-resistor-film-0805.step
│   ├── ...
├── ...
```

### Naming Convention

We adhere to a predetermined naming convention for ease of navigation and identification of models:

`<footprint-type>-<category>-<component>-<specifics>-<...>.<file-extension>`

The specifics part is optional.

Examples:
- A generic model: `smd-resistor-film-0603.step`.
- A generic model with specificities: `smd-capacitor-elec-d-6.3x5.4` (`d` representing the package type and `6.3x5.4` the diameter and height of the package).
- A model tied to a specific MPN: `th-connector-jack-acjs-mhdc` (`acjs-mhdc` being the part's MPN).

## Getting Started

### Prerequisites

This repository utilizes the Zippey script for handling FreeCAD sources in a Git-friendly manner. It needs to be set up on your machine if you plan to clone or contribute to this repository. Instructions can be found in this [this repo](https://github.com/ygn-effects/script-zippey).

Use the latest available version of FreeCAD if you need to work with the source files.

### Using the Models

The models have been exported from FreeCAD as `.step` files using the AP214 protocol, which should be compatible with most EDA packages.

## Contributing

We welcome contributions to the 3D Models Library. If you'd like to contribute, please:

- Open an issue using the Model request template.
    - Fill in the issue and include a screenshot of the diagram used as a reference.
- Fork the repository.
- Create a new branch for your contribution.
- Add your 3D models following the existing structure and naming conventions.
    - The model must be colorized.
    - You must include the FreeCAD source files.
    - The STEP file must be exported using the AP214 protocol.
- Submit a pull request with a clear description of your additions.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.
