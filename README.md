<div id="top"></div>

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/SolarSpec/GlobalFittingApp">
    <img src="GlobalFittingApp_resources/logo.png" alt="SolarSpec" width="160" height="120">
  </a>

<h3 align="center">GlobalFittingApp</h3>

  <p align="center">
    A Graphical User Interface 
    <br />
    <a href="https://github.com/SolarSpec/GlobalFittingApp"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/SolarSpec/GlobalFittingApp">View Demo</a>
    ·
    <a href="https://github.com/SolarSpec/GlobalFittingApp/issues">Report Bug</a>
    ·
    <a href="https://github.com/SolarSpec/GlobalFittingApp/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![GlobalFittingApp Screenshot][product-screenshot]](https://solarspec.ok.ubc.ca/)
Use MATLAB's Curve Fitting Toolbox and Global Optimization Toolbox to perform a problem-based, nonlinear-multivariate regression on your experimental data.
<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

* [MATLAB](https://www.mathworks.com/products/matlab.html)
* [Image Processing Toolbox](https://www.mathworks.com/help/images/)
<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To begin using this app is very simple. Just verify you have the necessary prequisites and follow the installation instructions.

### Prerequisites

Make sure MATLAB is installed. It is available for download in the Software Distribution section under the Help tab after you log into [Canvas.](https://canvas.ubc.ca/)
Click on the "Add-Ons" dropdown menu of your MATLAB Home screen. Then click on "Manage Add-Ons" and ensure you have the 'Optimization Toolbox', 'Symbolic Math Toolbox', 'Curve Fitting Toolbox' and 'Global Optimization Toolbox.' If not, click on "Get Add-Ons" button instead and search for the aforementioned products.

### Installation

1. Clone the repo to your PC
   ```sh
   git clone https://github.com/SolarSpec/GlobalFittingApp.git
   ```
2. Install the application 
   ```
   Click on the .mlappinstall file in your repository to open and install in MATLAB
   ```
3. Browse the APPS header
   ```
   You will find the recently installed application and can add it to your favourites
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage
To begin, import your data through either the Kinetics or Spectra buttons. You can also setup the solver, solver options and initial data beforehand instead. Below the load buttons, there is a radio button group that the user can use to include a Global Solver (GS): Global Search or Multi Start, or neither represented by "Off." Further down the left panel, we have the main solver dropdown menu that allows the user to choose which solver the problem-based solution will incorporate. Beside the dropdown is a push button that takes the user to the Global Solvers tab to allow any additional changes to the default objects. The tab menu will automatically switch to the selected dropdown solver when clicked. The user will not be able to manually change the tabs. The color dot at the bottom of the left panel lets the user know when the optimization is running.

In the middle panel the user can choose between using the application for fitting or spectra deconvolution as well. Since spectra deconvolution is not complete, we will focus on the first tab. The model presets dropdown allows the user to choose from a few options what the data model should look like but is not requried for the model editfield. The user has complete freedom with how they want to express the data's model by simply inputting the string form of their equation. However, there are a few cases that will cause an error in the app and so the user should also review the "MODEL EXAMPLES" push button at the button of the botttom left panel. The model is minimized through the non-linear least squares objective function. The push button "Optimize Globally" will initiate the optimization with all the current settings selected on the left panel and all the initial data from the right.

Furthermore, once an admissible model has been inputted, the app will then calculate the number of parameters and fill the editable table on the right panel with default values. Each parameter will require an initial guess, lower bound, upper bound, and a checkbox boolean value determining whether the selected parameter value is shared among multiple datasets. NOTE: The closer you are in your initial guesses to a properly scaled model, the better the outcome for an automatic optimization. Properly scaling your model is paramount to getting an optimization that not only converges on a solution, but the correct one. Without properly scaling your model, it is far easier to get trapped in local minima. If typicalX is selected in any solver that allows it, no initial guess must be exactly zero but it can be fairly close.

_For more information on any of the internal functions, please refer to the [MATLAB Documentation](https://www.mathworks.com/help/matlab/)_

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [X] Fit and plot 1-D data
- [X] Fit and plot N-D data
- [X] Express models graphically in mathematical expression
- [X] Allow generalization to input models
  - [ ] Perhaps add multiobjective capabilities if needed
- [ ] Include spectral decomposition

See the [open issues](https://github.com/SolarSpec/GlobalFittingApp/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the BSD 3-Clause License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

SolarSpec - [SolarSpec Website](https://solarspec.ok.ubc.ca/) - vidihari@student.ubc.ca

Project Link: [https://github.com/SolarSpec/GlobalFittingApp](https://github.com/SolarSpec/GlobalFittingApp)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Group Leader - Dr. Robert Godin](https://solarspec.ok.ubc.ca/people/)
* [The Entire SolarSpec Team](https://solarspec.ok.ubc.ca/people/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/SolarSpec/GlobalFittingApp.svg?style=for-the-badge
[contributors-url]: https://github.com/SolarSpec/GlobalFittingApp/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/SolarSpec/GlobalFittingApp.svg?style=for-the-badge
[forks-url]: https://github.com/SolarSpec/GlobalFittingApp/network/members
[stars-shield]: https://img.shields.io/github/stars/SolarSpec/GlobalFittingApp.svg?style=for-the-badge
[stars-url]: https://github.com/SolarSpec/GlobalFittingApp/stargazers
[issues-shield]: https://img.shields.io/github/issues/SolarSpec/GlobalFittingApp.svg?style=for-the-badge
[issues-url]: https://github.com/SolarSpec/GlobalFittingApp/issues
[license-shield]: https://img.shields.io/github/license/SolarSpec/GlobalFittingApp.svg?style=for-the-badge
[license-url]: https://github.com/SolarSpec/GlobalFittingApp/blob/main/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/haris-vidimlic-06730019b/
[product-screenshot]: GlobalFittingApp_resources/Screenshot.png
