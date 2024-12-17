# Personal Contextual Repository Data Pipeline (Github)

*18-Dec-24*

The purpose of this repository is to lay down some initial planning documentation for the implementation of a system for managing a structured pipeline for contextual data vectorization to improve the inference of large language models, especially assistants.

One of the ideas that I'm most motivated by in exploring large language models is the idea that users can assert ownership over a store of personal contextual data. 

[This repository](https://github.com/danielrosehill/Personal-Context-Repo-Idea) contains some similarly loose sketches describing how and why I think that users will need to take ownership over the long run over their contextual data. 

A  challenge inherent in the idea of organizing personal, contextual data, unlike, say, RAG pipelines for enterprise use, is that the data might be very small and very fragmented. 

As I noted in the idea repository linked above, there are also some idiosyncrasies about personal contextual data that distinguish it from other kinds of information of this nature. One of those is that if we do manage to codify the particulars of our life into some kind of a contextual store, we can expect that some elements of that datastore might remain essentially immutable, such as our city of birth for example, while others will be in a continuous state of flux, as are life circumstances similarly change.

Like others exploring the question of how best to organize personal contextual data at the moment, one of my guiding principles is that the pursuit of a perfect system shouldn't be an impediment to setting up a functional one. 

For that reason, my first attempts at implementing a personal contextual data store use the familiar comforts of a Github repository as a sort of "frontend", where the user can simply codify details of their personal or professional contexts at their leisure, organizing it in a folder system and then using that as a pipeline to feed the information into a vector database store. 

The repository above, the one outlining the high level overview of this idea, gives a sense for the type of data that I envision might be useful for both personal and professional use cases and also explains some examples of situations in which I think that small amounts of personal contextual data could be highly advantageous. 

## Architectural Plans

I plan to develop two specific pipeline architectures, both using a Github repository to vector database model. 

The first is a repository pipeline feeding into Open AI Assistants vector store. The first implementation will probably be a single repository to vector store pipeline. While a second implementation will implement some form of folder-based routing in which context data is organized in the files and folders of the repository, and those are routed into specific discrete vector stores within the Open AI platform.

To illustrate the envisioned functionality of the second implementation, a user might have two folders in their repository `personal data` and `work data` with the vectorization pipeline feeding the contents of each folder into different vector store endpoints; In this example, one presumably connected to a personal assistant or group of them, and the second connected to those used for professional purposes.

The second implementation idea Is using a Github repository to feed the contextual data into a Pipecone or Weaviate database or a self hosted vector database. This implementation would be more modular, with the pipeline feeding into the vector database, which is a detached unit from the large language model and deployment platform being used. 

This repository will probably be used just to sketch out some of these architectures, perhaps with some screenshots and diagrams.

## Author

Daniel Rosehill  
(public at danielrosehill dot com)

## Licensing

This repository is licensed under CC-BY-4.0 (Attribution 4.0 International) 
[License](https://creativecommons.org/licenses/by/4.0/)

### Summary of the License
The Creative Commons Attribution 4.0 International (CC BY 4.0) license allows others to:
- **Share**: Copy and redistribute the material in any medium or format.
- **Adapt**: Remix, transform, and build upon the material for any purpose, even commercially.

The licensor cannot revoke these freedoms as long as you follow the license terms.

#### License Terms
- **Attribution**: You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **No additional restrictions**: You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

For the full legal code, please visit the [Creative Commons website](https://creativecommons.org/licenses/by/4.0/legalcode).