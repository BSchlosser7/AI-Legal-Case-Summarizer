
<a id="readme-top"></a>

<h1 align="center">AI Legal Case Summarizer</h1>

  <p align="center">
    <h3 align="center">Project Description</h3>

This project builds an intelligent legal research pipeline that streamlines how case documents are stored, retrieved, and summarized. Users first create a centralized repository containing multiple legal cases, each saved as an individual document. These documents are then ingested into a Retrieval-Augmented Generation (RAG) system, enabling highly accurate retrieval of case-specific information—whether answering targeted legal questions or generating detailed, context-rich summaries.

For fast consumption, the long-form summaries produced by the RAG model can be passed into a Supervised Fine-Tuned (SFT) summarization model. This secondary model transforms verbose case analyses into extremely concise, high-quality summaries optimized for quick understanding and efficient retrieval. Together, this pipeline creates a powerful end-to-end solution for managing, querying, and digesting complex legal case information.
    <br />
    <br />
    <a href="https://github.com/github_username/repo_name"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/github_username/repo_name">View Demo</a>
    &middot;
    <a href="https://github.com/github_username/repo_name/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/github_username/repo_name/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
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


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

Steps to take before running RAG and SFT models
</br>
Before Rag
* 1. Download Premade RAG Document
  ```sh
  curl -L -o RAG-Ready Compiled Cases "https://drive.google.com/uc?export=download&id=1D8q-z9hhRvT3dunEMWhMFrq619x8oXCw"
  ```
* 2. Create any .txt document with case information
  ```sh
  Create a document with all case information and title it Compiled Cases RAG
  ```
Before SFT
* 1. Download SFT Training Document as a csv
  ```sh
  curl -L "https://drive.google.com/uc?export=download&id=1gQcQ0NQTQwiPxcm_0i6RedkbVM_vrggM" -o myfile.zip
  ```

Important Piece of Advice: When using Colab, use A100 GPU as selected runtime for max efficiency

### Running RAG Model

1. Open the [RAG colab notebook](https://colab.research.google.com/drive/1k775dmgq6Sw2-eLJWe3i02b2LYp-sHlA?usp=sharing)
2. Clone the notebook to your personal drive
3. Insert personal API and Class
   ```sh
   AZURE_API_KEY = "[Insert Here]"
   CLASS = "[Insert Here]"
   ```
4. Upload Compiled Cases RAG to current Colab Notebook
  * Left Sidebar --> File Icon --> Upload Icon --> Compiled Cases RAG
   
5. If you ADDED new cases or CHANGED existing ones, edit to include: 
   ```sh
   evaluate_questions = [
    "Write a case summary for Celotex Corp. v Catrett",
    "Write a case summary for Harrington v Richter",
    "Write a case summary for Bell v Cone",
    "Write a case summary for Lockyer v Andrade",
    "Write a case summary for Arizona v Evans",
    "Write a case summary for Maryland v King",
    "Write a case summary for Herring v US",
    "Write a case summary for [INSERT NEW CASE]
    ]
   ```
6. Click "Run all" in the menu bar and wait for outputs

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Running SFT Model
1. Open the [SFT colab notebook](https://colab.research.google.com/drive/1CqoHt73PNGU0aFp2-CS_liAiuYlqkeAj?usp=sharing)
2. Clone the notebook to your personal drive
3. Upload SFT Training Data to current Colab Notebook
  * Left Sidebar --> File Icon --> Upload Icon --> sftdata.csv
4. Click "Run all" in the menu bar and scroll to bottom of the colab notebook (this may take a couple minutes)
5. Paste the "Case Name" of the intended case
    ```sh
   Case Name = "[Insert Here]"
    ```
6. Paste the "Long Summary" outputted by the RAG model that aligns with the "Case Name"
    ```sh
   Long Summary = "[Insert Here]"
    ```
7. Press "Generate Short Summary" and wait for output






<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



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

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Top contributors:

<a href="https://github.com/github_username/repo_name/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=github_username/repo_name" alt="contrib.rocks image" />
</a>



<!-- LICENSE -->
## License

Distributed under the project_license. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email@email_client.com

Project Link: [https://github.com/github_username/repo_name](https://github.com/github_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo_name/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png
<!-- Shields.io badges. You can a comprehensive list with many more badges at: https://github.com/inttter/md-badges -->
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
