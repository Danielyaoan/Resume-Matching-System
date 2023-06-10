# Resume-Matching-System

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#something-to-improve">Something to Improve</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This project integrate the powerful GPT-3.5 engine with OpenAI-API to extract and summarize resume and job descriptions. [text-davinci-003](https://platform.openai.com/docs/models/gpt-3-5) model is selected due to its feature that can do any language task with better quality, longer output, and consistent instruction-following than the curie, babbage, or ada models.

To compute the similarity between resume and potential job openings, HuggingFace Transformers are selected. [sentence-transformers/paraphrase-MiniLM-L3-v2](https://huggingface.co/sentence-transformers/paraphrase-MiniLM-L3-v2) is selected due to its complexity in word embeddings as it is trained with a variety of data (AllNLI, sentence-compression, SimpleWiki, altlex, msmarco-triplets, quora_duplicates, coco_captions,flickr30k_captions, yahoo_answers_title_question, S2ORC_citation_pairs, wiki-atomic-edits, stackexchange_duplicate_questions), which allows it to accurately compute the similarity in different field and not limited to certain area.

Reseum data in this project only contains resume in technology domain, while job description include a variety of positions in multiple fields. Though I only make use of 2000 job description in this project as an example, there are over 285000 job description avaliable in data folder.

A final website is devised and deployed to local server as a prototype in this project. A simple demonstration of the website can be seen here 




https://github.com/Danielyaoan/Resume-Matching-System/assets/97267439/8dedb65d-8bbc-435f-ad4e-6a8dade30cef








<!-- GETTING STARTED -->
## Getting Started


### Dependencies

* requirement
```sh
pip install -qr requirements.txt
```

### Installation

1. Clone the repo
   ```sh
   https://github.com/Danielyaoan/Resume-Matching-System.git
   ```
2. All data are included in the following google drive: 

[https://drive.google.com/drive/folders/1FW6YmO4vEsaNNZPpUZqvEyMX-w4WfBBa?usp=sharing](https://drive.google.com/drive/folders/1FW6YmO4vEsaNNZPpUZqvEyMX-w4WfBBa?usp=sharing)



<!-- USAGE EXAMPLES -->
## Usage

Download all file in google cloud and install all dependencies. 
***Please go to openai api website and create your own openai api before running below files, note that using openai api may cost extra money when you exceed free credit.***
1. (Optional) Run the file ```Resume data analysis and classify performance comparison of different models.ipynb```
2. Run ```Data Preparation.ipynb``` to prepare file for next step
3. Run ```Job Description Summary.ipynb``` to summarize job description
4. (Optional) Run ```Resume Extraction.ipynb``` to extract important information from resume
5. (Optional) Run ```Matching Score with GPT-3.ipynb``` or ```Similarity Score.ipynb``` to compare similarity score between GPT-3.5 engine and HuggingFace Transformers. ***Note that computing similarity with GPT3.5 engine may cost you extra money***
6. Run ```APP.ipynb``` to deployed a website in your local server



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- SOMETHING TO IMPROVE -->
## Something to Improve

1. Due to the high cost of openai-api, using GPT-3.5 engine to extract resume and job description could lead to an amount of money. As a result, I only select a few existing job openings to be as example for demonstration in this project. If money is not a problem, web scraping is definitely a technique to use in this project that allow users to compare their resume with real-time job openings.
2. Due to the limit amount of memory availabe in AWS EC2 free tier server, libraries are too large to install in the environment. If budget allows, website in this project could deployed with AWS EC2 and S3 to make it availabe with public.
3. The computational time of HuggingFace Transformers is too large with limited usage of GPU in my personal computer. If available, run this project in a higher performance computer could significantly reduce the computational time.

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- Authors -->
## Authors

Yao An Lee - danielyaoanlee@gmail.com

Project Link: [https://github.com/Danielyaoan/Resume-Matching-System.git](https://github.com/Danielyaoan/Resume-Matching-System.git).


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements



## Thank you
