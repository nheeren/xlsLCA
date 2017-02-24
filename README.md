# xlsLCA

> **Under construction. Code & more details will follow.**

`xlsLCA` is a tool to perform [life-cycle-assessment](https://en.wikipedia.org/wiki/Life-cycle_assessment) (LCA) using Excel files. It aims at simplifying the LCA process by providing the user a relatively simple modeling environment.

`xlsLCA` builds on the powerful [brightway2](https://brightwaylca.org/) (bw2) Python LCA framework by Chris Mutel and aims at simplifying LCA impact assessment.

The project was initially developed to perform the LCA calculations in the publication by Kristjansdottir et al. 201?.

## Usage

The tool consist of an Excel file that is used for linking user-defined processes and a [Jupyter notebook](http://jupyter.org/) to perform linking and calculations.

The repository contains an example file.

### Linking (Excel file)

The Excel file has variable process depth, each represented by a separate sheet. The linking tool will create a bw2 database based on the entries of the Excel sheets.

The example file contains the following sheets: `building`, `element`, and `material`.

To define a building inventory it is necessary to create entries (lines) in the `building` sheet. For instance:

| Name       | amount | sub-process |
|------------|--------|-------------|
| Building A | 20     | Wall North  |
| Building A | 30     | Wall East   |
| Building A | 20     | Wall South  |

So each line represents an inventory item of `Building A`. The inventories of the sub-elements are defined in the next level, which is the sheet `elements` in this case. It could also be defined in the same sheet, but we chose this structure for more clarity.

All self-defined processes are defined following that method. Although circular references are possible, all processes must be linked to a life cycle database process (e.g. ecoinvent) eventually.

### Impact assessment

## Installation

    TODO

## Outlook

## License

    TODO

## Credits

The tool was developed by Niko Heeren at the chair of [Ecological System Design](http://www.esd.ifu.ethz.ch/). Further contributors are:

- Torhildur Kristjansdottir
- Mélanie Haupt
