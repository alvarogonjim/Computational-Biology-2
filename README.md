

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h3 align="center">Salmonella Outbreak</h3>
  <p align="center">
    Provide a set of tools to analize two simple FASTA sequencing files (reads) and outputs a list of SNPs in the case of Salmonella.
    <br />
    <a href="http://alvarogj.me/static/media/Salmonella-outbreak.f49c4349.pdf"><strong>Read the Computational-Biology-2»</strong></a>
    <br />
    <br />
    ·
    <a href="https://github.com/alvarogonjim/Computational-Biology-2/issues">Computational-Biology-2 Bug</a>
    ·
    <a href="https://github.com/alvarogonjim/Computational-Biology-2/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Getting Started](#getting-started)
  * [Installation](#installation)
* [Usage](#usage)
  * [K-mers module](#module-k-mers)
  * [SNPs module](#module-snps)
  * [Protein structure module](#module-protein-structure)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About The Project
This project correspond to the second project of the course of [Computational Biology](https://clovisg.github.io/teaching/protein-structure-prediction/session1.html).
We had to provide different tools in case of a Salmonella outbreak. 


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Installation
 
1. Clone the Computational-Biology-2
```sh
git clone https://github.com/alvarogonjim/Computational-Biology-2.git
```
2. Install Python packages
```sh
pip install -r requirements.txt
```


<!-- USAGE EXAMPLES -->
## Usage

### Module k-mers

This module calculates the k-mers of a specific FASTA file. The output of this module is a dictionary
that contains the subsequences and the number of times that this subsequences is repeated in the whole
input file, the dictionary will be serialized as a Pickle file 

```sh
python3 kmers.py -i salmonella-enterica.reads.fna -o kmers_1 -k 15
```

- -h, --help shows a help message and exit
- -i, --fasta name of the FASTA file that we want to calculate the k-mers. This file must be in the
directory of the project.
- -o, --output name of the Pi
- -k, size of the k-mers. By default this value is 15.


### Module SNPs

This module two dictionary of k-mers stored in Pickle format and outputs a list of SNPs


```sh
python3 snp.py -kmers kmers_0.pkl -kmers2 kmers_1.pkl -k 15
```

- -h, --help shows a help message and exit
- -kmers, --kmers_file name of the Pickle file that contains the k-mers of the first sequence. This
file must be in the directory of the project.
- -kmers2, --kmers_file2 name of the Pickle file that contains the k-mers of the second sequence.
This file must be in the directory of the project.
- -k, size of the k-mers. By default this value is 15.


### Module protein structure

This module takes a multiple sequence alignment in standard FASTA file format and outputs the contact
matrix in the required format to be executed by FT-COMAR software.

- -h, --help shows a help message and exit
- -i, --fasta name of the multiple sequence alignment FASTA file. This file must be in the directory
of the project.
- -o, --output name of the file to store the contact matrix and be used in FT-COMAR software. By
default the name is cmatrix.
- -t, Threshold to compute the contact matrix. By default this value is 0.01.




<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Álvaro González Jiménez - [website](https://alvarogj.me) - alvarogonjim95@gmail.com

Project Link: [https://github.com/alvarogonjim/Computational-Biology-2](https://github.com/alvarogonjim/Computational-Biology-2)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [BATIER Lucas](https://www.linkedin.com/in/lucasbat/)
* [PILIPOVIC Predrag](https://www.linkedin.com/in/predrag-pilipovic-50938212a/)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
