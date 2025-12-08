
<a id="readme-top"></a>

<h1 align="center">AI Legal Case Summarizer</h1>

  <p align="center">
    <h3 align="center">Project Description</h3>

This project builds an intelligent legal research pipeline that streamlines how case documents are stored, retrieved, and summarized. Users first create a centralized repository containing multiple legal cases, each saved as an individual document. These documents are then ingested into a Retrieval-Augmented Generation (RAG) system, enabling highly accurate retrieval of case-specific information—whether answering targeted legal questions or generating detailed, context-rich summaries.

For fast consumption, the long-form summaries produced by the RAG model can be passed into a Supervised Fine-Tuned (SFT) summarization model. This secondary model transforms verbose case analyses into extremely concise, high-quality summaries optimized for quick understanding and efficient retrieval. Together, this pipeline creates a powerful end-to-end solution for managing, querying, and digesting complex legal case information.
    <br />
    <br />
    <br />
    <br />
    <a href="https://github.com/github_username/repo_name">View Demo</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#Running-RAG-Model">Running RAG Model</a></li>
        <li><a href="#Running-SFT-Model">Running SFT Model</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#techniques-used">Techniques Used</a></li>
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

This project is designed to function as a practical research assistant for legal professionals, helping them quickly navigate complex case material and retrieve exactly what they need in seconds. By storing case documents in a centralized repository, lawyers can query their entire library with natural language questions and receive precise, citation-ready responses.

<h3 align="left">How Lawyers Use the Tool</h3>

Fast Case Familiarization:
When preparing for hearings, depositions, or client meetings, attorneys can request concise summaries of any case in their library. This eliminates the need to skim lengthy opinions and accelerates early-stage research.

Targeted Legal Questions:
Lawyers can ask highly specific questions such as “What did the Court say about federal taxation powers in McCulloch v. Maryland?”
The RAG model retrieves only the relevant sections—saving time and reducing the risk of overlooking important details.

Consistent Summary Formatting:
The SFT model outputs all summaries in a uniform, structured format, making it easy to build case binders, research memos, or internal knowledge systems.

Efficient Multi-Case Comparison:
Because each summary follows the same template, attorneys can quickly compare holdings, plaintiffs/defendants, and legal principles across different cases.

<h3 align="left">Example Output</h3>

Below is an example of a summary lawyers would receive from the SFT model:
```sh
  McCulloch v. Maryland
  Year: 1819
  Plaintiff: State of Maryland
  Defendant: James McCulloch
  Summary: The Court ruled that Congress had implied powers and states could not tax federal institutions.
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Techniques Used

- [ ] Technique 1: Retrieval Augmented Generation (RAG)
    * RAG combines document retrieval with generative AI to provide accurate, context-grounded answers. Instead of relying on the model’s memory alone, it searches your case repository, pulls the most relevant excerpts, and uses them to generate precise legal responses or long-form summaries.
- [ ] Technique 2: Supervised Fine Tuning (SFT)
    * SFT trains a model on curated examples to produce consistent, high-quality outputs in a specific style. In this project, the SFT model learns to turn lengthy case explanations into short, structured, attorney-ready summaries for fast review and comparison.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTACT -->
## Contact

Team LAB MIS372T 

- Brady Schlosser: bradyschlosser@utexas.edu

- Anika Filitz: anikafilitz@utexas.edu

- Lucia Bonnin: luciabonnin@utexas.edu

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* We would like to thank our Professor, Yan Leng, and our two Teaching Assistants, Yunxin Sang and Yang Zhao, who helped us
  throughout the entire project and semester.

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
