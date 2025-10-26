# llm-gpt4all-Installation


**STEPS:**

python3 -m venv ~/venv   <======= ENTER ENV if needed

source ~/venv/bin/activate   <==== ACTIVATE

pip install llm

NOTE: If Python3 and venv not available install them.


deactivate  <==== to DEACTIVATE


llm models list

llm install llm-gpt4all

llm models list



**SELECT THE MODEL TO INSTALL:**



| Model                                                                                   | Size / RAM approx    | Licence notes                                                             | Good for                                                      |
| --------------------------------------------------------------------------------------- | -------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------- |
| Phi‑3 Mini Instruct (~4 B parameters, 2.18 GB download, needs ~4 GB RAM) ([GPT4All][1]) | Light / low resource | MIT licence (makes commercial use easier) ([GPT4All][1])                  | Smaller laptops / testing / simple chat                       |
| Mini Orca (Small) (~3 B parameters, ~1.98 GB download, ~4 GB RAM) ([GPT4All][1])        | Very light           | CC-BY-NC-SA-4.0 (so non-commercial) ([GPT4All][1])                        | Experimentation, low-resource machine                         |
| Llama 3 Instruct (8 B parameters, ~4.66 GB download, ~8 GB RAM) ([GPT4All][1])          | Mid-level hardware   | Owned by Meta, license may restrict commercial use (check) ([GPT4All][1]) | Better performance if your machine supports it                |
| GPT4All Snoozy (13 B parameters, ~7.37 GB download, ~16 GB RAM) ([GPT4All][1])          | High resource        | GPL licence (so open-source) ([GPT4All][1])                               | If you have a beefy laptop/desktop, want stronger performance |

[1]: https://docs.gpt4all.io/gpt4all_desktop/models.html?utm_source=chatgpt.com "Download Models - GPT4All Documentation"


**OPEN AI KEY:**

Add one using 'llm keys set openai' or set the OPENAI_API_KEY environment variable

**OR**

export OPENAI_API_KEY="sk-your_api_key_here"

To make that permanent, you can add the export line to your shell config file (~/.bashrc, ~/.zshrc, etc.).




**To Chat with a Model:**

llm -m gpt4all-13b-snoozy-q4_0 'hi'

llm chat -m orca-mini-3b-gguf2-q4_0


**Removing Models:**

To remove a downloaded model, delete the .gguf file from ~/.cache/gpt4all

**SET DEFAULT MODEL:**

llm models default gpt4all-13b-snoozy-q4_0
