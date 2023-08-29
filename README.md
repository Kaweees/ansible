<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<div align="left">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]

</div>

<a href="https://github.com/Kaweees/ansible">
  <source media="(prefers-color-scheme: dark)" srcset="assets/img/ansible-logo-light-mode.png">
  <img alt="Text changing depending on mode. Light: 'Ansible Logo Light Mode' Dark: 'Ansible Logo Dark Mode'" src="assets/img/ansible-logo-dark-mode.png" align="right" width="150">
</a>

<div align="left">
  <h1><em>~ansible</em></h1>
</div>

<!-- ABOUT THE PROJECT -->
This playbook installs most of the software I use on my Linux machine for software development. This is a work-in-progress, and things will probably change as the sands of time flow.

### Built With
[![Ansible][Ansible-shield]][Ansble-url]

<!-- GETTING STARTED -->
## Getting Started

To get a local copy of the project up and running on your machine, follow these simple steps:


### Installation

It is best to run this playbook remotely, as it is designed to be executed on a fresh install of Linux. To do so, run the following command:

```bash
bash < <(curl -s https://raw.githubusercontent.com/Kaweees/ansible/main/ansible-install)
```

Enter your machine's password when prompted.

<!-- USAGE EXAMPLES -->
## Usage

### Running

###  Testing

Testing this playbook locally can be done by following the steps below:

1. Clone the repository
   ```bash
    git clone https://github.com/Kaweees/ansible.git
    cd ansible
    ```
2. Install Ansible via pip
    ```bash
    pip install ansible
    ```
3. Install Molecule with Docker support via pip
    ```bash
    pip install molecule[docker]
    ```
4. Initialize a Molecule scenario locally with Docker as the driver
    ```bash
    molecule init scenario -r local -d docker
    ```
5. Run the Molecule tests with the initialized scenario
    ```bash
    molecule test
    ```

<!-- ROADMAP -->
## Roadmap

See the [open issues](

<!-- PROJECT FILE STRUCTURE -->
## Project Structure

```
. ansible/
├── .ssh                      - ssh configuration files
├── auth_codes                - auth codes for various services
├── meta                      - metadata regarding this project for Ansible Galaxy
├── molecule                  - molecule tests
│   └── default
│       ├── converge.yml      - main ansible playbook
│       ├── molecule.yml      - molecule configuration
│       └── verify.yml        - molecule verification
├── tasks                     - various ansible tasks
├── README.md                 - you are here
├── ansible-run               - entry point that install ansible and runs the playbook
└── local.yml                 - ansible playbook to run locally
```

<!-- LICENSE -->
<!-- https://choosealicense.com/ -->
## License

My ansible scripts are distributed under the terms of the GNU General Public License v3.0, as I firmly believe that collaborating on free and open-source software fosters innovations that mutually and equitably beneficial to both collaborators and users alike. See [LICENSE](LICENSE) for details and more information.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/Kaweees/ansible.svg?style=for-the-badge
[contributors-url]: https://github.com/Kaweees/ansible/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Kaweees/ansible.svg?style=for-the-badge
[forks-url]: https://github.com/Kaweees/ansible/network/members
[stars-shield]: https://img.shields.io/github/stars/Kaweees/ansible.svg?style=for-the-badge
[stars-url]: https://github.com/Kaweees/ansible/stargazers

<!-- MARKDOWN SHIELD BAGDES & LINKS -->
[Ansible-shield]: https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=FFFFFF&labelColor=222222&color=FFFFFF
[Ansble-url]: https://www.ansble.com
