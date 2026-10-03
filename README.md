# BrushQuadX Drone Documentation

This documentation provides design, development, and implementation details of the brush quadcopter drone. 

## Documentation

The documentation that provides more details and tutorials on building the drone can be found under `\docs`. 

To generate the documentation using `sphinx`, follow the tutorial below with the command line. 

```shell
pip install -r requirements.txt
```

```shell
cd docs
```

### Windows (PowerShell)

```powershell
.\make.bat clean
.\make.bat html
```

### Linux/macOS

```bash
make clean
make html
```

### Windows (PowerShell)

Install MiKTeX and Strawberry Perl (`latexmk` requires Perl on Windows):

```powershell
winget install --id MiKTeX.MiKTeX -e
winget install --id StrawberryPerl.StrawberryPerl -e
```

After installation, reopen PowerShell. In MiKTeX Console, update the package database, enable installation of missing packages, and install the `latexmk` package. Confirm that `perl --version` and `latexmk --version` work in PowerShell. Then build the PDF from the `docs` directory:

```powershell
.\make.bat latexpdf
```

### Linux

Install the LaTeX dependencies and build the PDF from the `docs` directory:

```bash
sudo apt-get install latexmk
sudo apt-get install texlive-fonts-recommended
sudo apt-get install texlive-latex-extra
make latexpdf
```
