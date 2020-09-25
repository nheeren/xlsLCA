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

## Installation

    TODO

## Outlook

## License

This code can be used under the [MIT license](https://choosealicense.com/licenses/mit/).

    Copyright (c) 2018, Niko Heeren (ETH Zurich)

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

## Credits

The tool was developed by Niko Heeren at the chair of [Ecological System Design](http://www.esd.ifu.ethz.ch/). Further contributors are:

- Torhildur Kristjansdottir
- Mélanie Haupt
