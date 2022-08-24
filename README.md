# A Survey on Biomedical Text Summarisation with Pre-trained Language Model(PLM)s

![](https://img.shields.io/badge/Status-building-brightgreen) ![](https://img.shields.io/badge/PRs-Welcome-red) 


# Resource
This repository contains a list of papers, codes, and datasets in Biomedical Text Summarisation based on PLM. If you found any errors, please don't hesitate to open an issue or pull a request.

<!--
If you find this repository helpful for your work,  please consider citing our survey paper. The Bibtex are listed below:
<pre>

</pre>
-->


## Contributor


Resource Contributed by [Qianqian Xie](), [Zheheng Luo](),  [Benyou Wang](),[Sophia Ananiadou](https://www.research.manchester.ac.uk/portal/sophia.ananiadou.html).

## Introduction

Biomedical text summarization has long been a fundamental task in biomedical natural language processing (BioNLP),
aiming at generating concise summaries that distil key information from one or multiple biomedical documents. In recent years,
pre-trained language models (PLMs) have been the de facto standard of various natural language processing tasks in the general
domain. Most recently, PLMs have been further investigated in the biomedical domain and brought new insights into the biomedical text
summarization task. 

To help researchers quickly grasp the development in this task and inspire further research, we line up available datasets, recent approaches and evaluation methods in this project.

At present, the project has been completely open source, including:

1. **BioTS dataset table:** we listed the datasets in the BioTS field, You can find the category, size, content, and access of them in the table.
2. **PLM Based BioTS Methods:** we classified and arranged papers based on the type of output summary, numbers and type of input documents. the current mainstream frontiers. Each line of the table contains the category, the strategy of applying PLM, the backbone model, the training type, and used datasets.
3. **BioTS Evaluation:** we listed metrics that cover three essential aspects in the evaluation of biomedical text summarization: 1) relevancy 2) fluency 3) factuality.

The organization and our survey and the detailed background of biomedical text summarization are illustrated in the pictures below.


![survey-overview](./pics/OverviewOfBiomedicalTextSummarizationWithPLM.png)


![BTSwPLMs-taxonomy](./pics/TaxonomyOfMethods.png)


## Quick path
- [Survey Paper](#survey-paper)
- [Dataset](#dataset)
- [Methods](#methods)
- [Evaluation](#evaluation)
- [Leading Board](#leadingboard)

## Survey Paper
1. **Text summarization in the biomedical domain: A systematic review of recent research** `J. biomedical informatics 2014` [[html]](https://www.sciencedirect.com/science/article/pii/S1532046414001476)
1. **Summarization from medical documents: a survey** `Artif. intelligence medicine 2005` [[html]](https://www.sciencedirect.com/science/article/pii/S0933365704001320)
1. **Automated methods for the summarization of electronic health records** `J Am Med Inform Assoc. 2015` [[html]](https://pubmed.ncbi.nlm.nih.gov/25882031/)
1. **A systematic review of automatic text summarization for biomedical literature and ehrs** `J Am Med Inform Assoc. 2021` [[html]](https://pubmed.ncbi.nlm.nih.gov/34338801/)

## Dataset
<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th>Name</th>
    <th>Category</th>
    <th>Size</th>
    <th>Content</th>
    <th>Multi/Single Sum(M/S)</th>
    <th>Access</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> PubMed </td></code>
		<td> Biomedical literature </td>
		<td> 133,215 </td>
		<td> Full contents of articles</td>
		<td> Single </td>
		<td> <a href="https://github.com/armancohan/long-summarization">https://github.com/armancohan/long-summarization</a></td>

<tr>
	<td><code> RCT                              </td></code>
		<td> Biomedical literature </td>
		<td> 4,528 </td>
		<td> Titles and abstracts of articles</td>
		<td> Multiple </td>
		<td> <a href="https://github.com/bwallace/RCT-summarization-data">https://github.com/bwallace/RCT-summarization-data</a></td>
<tr>
	<td><code> MSˆ2                               </td></code>
		<td> Biomedical literature </td>
		<td> 470,402 </td>
		<td> Abstracts of articles</td>
		<td> Multiple </td>
		<td> <a href="https://github.com/allenai/ms2/">https://github.com/allenai/ms2/</a></td>
<tr>
	<td><code> CDSR                               </td></code>
		<td> Biomedical literature </td>
		<td> 7,805 </td>
		<td> Abstracts of articles</td>
		<td> Single </td>
		<td> <a href="https://github.com/qiuweipku/Plain language summarization">https://github.com/qiuweipku/Plain language summarization</a></td>
<tr>
	<td><code> SumPubMed                               </td></code>
		<td> Biomedical literature </td>
		<td> 33,772 </td>
		<td> Full contents of articles</td>
		<td> Single </td>
		<td> <a href="https://github.com/vgupta123/sumpubmed<">https://github.com/vgupta123/sumpubmed</a></td>
<tr>
	<td><code>S2ORC                              </td></code>
		<td> Biomedical literature </td>
		<td> 63,709 </td>
		<td> Full contents of articles </td>
		<td> Single </td>
		<td> <a href="https://github.com/jbshp/GenCompareSum<">https://github.com/jbshp/GenCompareSum</a></td>
<tr>
	<td><code> CORD-19                               </td></code>
		<td> Biomedical literature </td>
		<td> - (constantly increasing)</td>
		<td> Full contents of articles</td>
		<td> Single </td>
		<td> <a href="https://github.com/allenai/cord19<">https://github.com/allenai/cord19</a></td>
<tr>
	<td><code> MIMIC-CXR                              </td></code>
		<td> EHR</td>
		<td> 124577</td>
		<td> Full contents of reports</td>
		<td> Single </td>
		<td> <a href="https://physionet.org/content/mimic-cxr/2.0.0/<">https://physionet.org/content/mimic-cxr/2.0.0/</a></td>
<tr>
	<td><code> OpenI                              </td></code>
		<td> EHR</td>
		<td> 3599</td>
		<td> Full contents of reports</td>
		<td> Single </td>
		<td> <a href="https://openi.nlm.nih.gov/faq#collection<">https://openi.nlm.nih.gov/faq#collection</a></td>
<tr>
	<td><code> MeQSum                              </td></code>
		<td> meidical question summarization</td>
		<td> 1000</td>
		<td> Full contents of question</td>
		<td> Single </td>
		<td> <a href="https://github.com/abachaa/MeQSum<">https://github.com/abachaa/MeQSum/</a></td>
<tr>
	<td><code> CHQ-Summ                               </td></code>
		<td> meidical question summarization</td>
		<td> 1507</td>
		<td> Full contents of question</td>
		<td> Single </td>
		<td> <a href="https://github.com/shwetanlp/Yahoo-CHQ-Summ<">https://github.com/shwetanlp/Yahoo-CHQ-Summ</a></td>
<tr>
</tbody >
</table>
</div>


## Methods
<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th>Paper</th>
    <th>Category</th>
    <th>Strategy</th>
    <th>Model</th>
    <th>Training</th>
    <th>Dataset</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code><a href="https://arxiv.org/pdf/2007.03405.pdf"> ContinualBERT </a></code><a href="https://github.com/jdubpark/continual-bert"> [code] </a></td>
		<td>extractive</td>
		<td> fine-tuning</td>
		<td> BERT</td>
		<td> supervised </td>
		<td> PubMed, CORD-19</td>

<tr>
	<td><code><a href="https://www.sciencedirect.com/science/article/abs/pii/S0950705120302859"> BioBERTSum </a> </td></code>
		<td> extractive </td>
		<td>fine-tuning </td>
		<td> BioBERT</td>
		<td> supervised </td>
		<td> PubMed</td>
<tr>
	<td><code> <a href="https://www.sciencedirect.com/science/article/pii/S0950705122007328"> KeBioSum </a> </code> <a href="https://github.com/xashely/KeBioSum"> [code] </a> </td>
		<td> extractive </td>
		<td> adaption+fine-tuning </td>
		<td> PubMedBERT</td>
		<td> supervised </td>
		<td> PubMed, CORD-19, S2ORC</td>
<tr>
	<td><code>    <a href="	https://arxiv.org/pdf/2104.08942.pdf"> N. Kanwal and G. Rizzo</a></code> <a href="https://github.com/NeelKanwal/BERTOLOGY-Based-Extractive-Summarization-for-Clinical-Notes"> [code]</a></td>
		<td> extractive </td>
		<td> fine-tuning </td>
		<td> BERT</td>
		<td> unsupervised </td>
		<td> MIMIC-III</td>
<tr>
	<td><code>      <a href="https://www.researchgate.net/profile/Milad-Moradi-5/publication/336272974_Deep_contextualized_embeddings_for_quantifying_the_informative_content_in_biomedical_text_summarization/links/5d9c45d3a6fdccfd0e811d95/Deep-contextualized-embeddings-for-quantifying-the-informative-content-in-biomedical-text-summarization.pdf"> M. Moradi et.al   </a></code> <a href="https://github.com/BioTextSumm/BERT-based-Summ"> [code]</a></td>
		<td> extractive </td>
		<td> feature-base </td>
		<td> BERT </td>
		<td> unsupervised </td>
		<td> PubMed</td>
<tr>
	<td><code>      <a href="https://www.sciencedirect.com/science/article/pii/S1532046420300800"> M. Moradi et.al</a> </code> <a href="https://github.com/BioTextSumm/Graph-basedSummarizer"> [code]</a></td>
		<td> extractive </td>
		<td> feature-base</td>
		<td> BioBERT</td>
		<td> unsupervised </td>
		<td> PubMed</td>
<tr>
	<td><code>  <a href="https://aclanthology.org/2022.bionlp-1.22/">   GenCompareSum    </a></code> <a href="https://github.com/jbshp/GenCompareSum"> [code]</a></td>
		<td> extractive</td>
		<td> feature-base</td>
		<td> T5</td>
		<td> unsupervised </td>
		<td> PubMed, CORD-19, S2ORC</td>
<tr>
	<td><code> <a href="https://pubmed.ncbi.nlm.nih.gov/35923376/">   RadBERT    </a></td></code> </td></code>
		<td> extractive</td>
		<td> feature-base</td>
		<td> RadBERT</td>
		<td> unsupervised </td>
		<td> - </td>
<tr>                                                                                                                                                                                          
        <td><code><a href="https://arxiv.org/pdf/2006.01997.pdf">   B Tan et.al  </a></code> <a href="https://github.com/VincentK1991/BERT_summarization_1"> [code]</a></td>                                                                                                                               
                <td>hybrid</td>                                                                                                                                                               
                <td>adaption+fine-tuning</td>                                                                                                                                                 
                <td>BERT,GPT-2</td>                                                                                                                                                           
                <td>supervised</td>                                                                                                                                                           
                <td>CORD-19</td>                                                                                                                                                              
<tr>                                                                                                                                                                                          
        <td><code> <a href="https://arxiv.org/pdf/2005.00163.pdf">S. S. Gharebagh et.al</a></td></code>                                                                                                                                  
                <td>abstractive</td>                                                                                                                                                          
                <td>feature-base</td>                                                                                                                                                         
                <td>BERT</td>                                                                                                                                                                 
                <td>supervised</td>                                                                                                                                                           
                <td>MIMIC-CXR</td>                                                                                                                                                            
<tr>                                                                                                                                                                                          
        <td><code>  <a href="https://ojs.aaai.org/index.php/AAAI/article/view/16089/15896">Y. Guo et.al </a> </code> <a href="https://github.com/qiuweipku/Plain_language_summarization "> [code]</a></td>                                                                                                                                                                                                                                                    
                <td>hybrid</td>                                                                                                                                                               
                <td>adaption+fine-tuning</td>                                                                                                                                                 
                <td>BERT, BART</td>                                                                                                                                                           
                <td>supervised</td>                                                                                                                                                           
                <td>CDSR</td>                                                                                                                                                                 
<tr>                                                                                                                                                                                       
        <td><code><a href="https://aclanthology.org/2021.bionlp-1.29/">L. Xu et.al </a></td></code>                                                                                                                                     
                <td>abstractive,question</td>                                                                                                                                                 
                <td>adaption+fine-tuning</td>                                                                                                                                                 
                <td>BART,PEGASUS</td>                                                                                                                                                         
                <td>supervised</td>                                                                                                                                                           
                <td>MIMIC-CXR,OpenI,MeQSum</td>                                                                                                                                               
<tr>                                                                                                                                                                                          
        <td><code> <a href="https://aclanthology.org/2021.bionlp-1.10.pdf">W. Zhu et.al</a>   </td></code>
                <td>abstractive</td>
                <td>fine-tuning</td>
                <td>BART,T5,PEGASUS</td>
                <td>supervised</td>
                <td>MIMIC-CXR,OpenI</td>
<tr>
        <td><code>  <a href="https://aclanthology.org/2021.bionlp-1.32.pdf"> R. Kondadadi et.al </a></td></code>
                <td>abstractive</td>
                <td>fine-tuning</td>
                <td>BART,T5,PEGASUS</td>
                <td>supervised</td>
                <td>MIMIC-CXR,OpenI</td>
<tr>
        <td><code><a href="https://aclanthology.org/2021.bionlp-1.11.pdf">S. Dai et.al</a></td></code>
                <td>abstractive</td>
                <td>adaption+fine-tuning</td>
                <td>PEGASUS</td>
                <td>supervised</td>
                <td>MIMIC-CXR,OpenI</td>
<tr>
        <td><code><a href="https://aclanthology.org/2021.bionlp-1.35.pdf">  D. Mahajan et.al</a></td></code>
                <td>abstractive</td>
                <td>adaption+fine-tuning</td>
                <td><a href="https://aclanthology.org/2020.tacl-1.18/">BioRoBERTa</a></td>
                <td>supervised</td>
                <td>MIMIC-CXR,OpenI</td>
<tr>
        <td><code><a href="https://aclanthology.org/2022.acl-long.320.pdf">H. Jingpeng et.al </a></code> <a href="https://github.com/jinpeng01/AIG_CL"> [code]</a></td>                   
        		   <td>abstractive</td>
                <td>fine-tuning</td>
                <td>BioBERT</td>
                <td>supervised</td>
                <td>MIMIC-CXR,OpenI</td>
<tr>
        <td><code> <a href="https://www.sciencedirect.com/science/article/pii/S1532046422000156 ">X. Cai et.al </a></td></code>
                <td>abstractive</td>
                <td>fine-tuning</td>
                <td>SciBERT</td>
                <td>supervised</td>
                <td>CORD-19</td>
<tr>
        <td><code>   <a href="https://arxiv.org/pdf/2204.02208"> A. Yalunin et.al </a></td></code>
                <td>abstractive</td>
                <td>adaption+fine-tuning</td>
                <td>BERT,Longformer</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8378607/">  B. C. Wallace et.al</a></code> <a href="https://github.com/bwallace/RCT-summarization-data"> [code]</a></td>           
                <td>abstractive,multi-doc</td>
                <td>adaption+fine-tuning</td>
                <td>BART</td>
                <td>supervised</td>
                <td>RCT</td>
<tr>
        <td><code>   <a href="https://arxiv.org/pdf/2104.06486">  J. DeYoung et.al</a></code> <a href="https://github.com/allenai/ms2"> [code]</a></td> 
                <td>abstractive,multi-doc</td>
                <td>fine-tuning</td>
                <td>BART,Longformer</td>
                <td>supervised</td>
                <td>MSˆ2</td>
<tr>
        <td><code>  <a href="https://www.nature.com/articles/s41746-021-00437-0">A. Esteva et.al </a></td></code>
                <td>abstractive,multi-doc</td>
                <td>fine-tuning</td>
                <td>BERT,GPT-2</td>
                <td>supervised</td>
                <td>CORD-19</td>
<tr>
        <td><code><a href="https://aclanthology.org/2020.nlpcovid19-2.14.pdf">CAiRE-COVID</a></code> <a href="https://github.com/HLTCHKUST/CAiRE-COVID"> [code]</a></td> 
                <td>hybrid,multi-doc</td>
                <td>fine-tuning,feature-base</td>
                <td>ALBERT,BART</td>
                <td>un+supervised</td>
                <td>CORD-19</td>
<tr>
        <td><code><a href="https://aclanthology.org/2020.coling-main.63.pdf">HET</a></code> <a href="https://github.com/cuhksz-nlp/HET-MC"> [code]</a></td> 
                <td>extractive,dialogue</td>
                <td>fine-tuning</td>
                <td>BERT</td>
                <td>supervised</td>
                <td>HET-MC</td>
<tr>
        <td><code><a href="https://aclanthology.org/2021.acl-long.384.pdf">CLUSTER2SENT</code> <a href="https://github.com/acmi-lab/modular-summarization"> [code]</a></td> 
                <td>abstractive,dialogue</td>
                <td>fine-tuning</td>
                <td>BERT,T5</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href="https://www.cs.cmu.edu/~mgormley/papers/zhang+al.emnlp.2021.pdf">L. Zhang et.al </a> </code> <a href="https://github.com/negrinho/medical_conversation_summarization"> [code]</a></td> 
                <td>abstractive,dialogue</td>
                <td>fine-tuning</td>
                <td>BART</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href='https://aclanthology.org/2021.nlpmc-1.9.pdf'>B. Chintagunt et.al</a></td></code>
                <td>abstractive,dialogue</td>
                <td>fine-tuning</td>
                <td>GPT-3</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href='https://aclanthology.org/2022.naacl-srw.32.pdf'>  D. F. Navarro et.al</a></td></code>
                <td>abstractive,dialogue</td>
                <td>fine-tuning</td>
                <td>BART,T5, PEGASUS</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href='https://aclanthology.org/2022.bionlp-1.9.pdf'>BioBART</a></code> <a href="https://github.com/GanjinZero/BioBART"> [code]</a></td> 
                <td>abstractive,dialogue</td>
                <td>fine-tuning</td>
                <td>BioBART</td>
                <td>supervised</td>
                <td>-</td>
<tr>
        <td><code><a href='https://aclanthology.org/2021.bionlp-1.12.pdf'>Y. He et.al</a></td></code>
                <td>abstractive,question</td>
                <td>fine-tuning</td>
                <td>BART,T5,PEGASUS</td>
                <td>supervised</td>
                <td>MeQSum,MIMIC-CXR,OpenI</td> 
<tr>
        <td><code><a href='https://aclanthology.org/2021.acl-short.33.pdf'>S. Yadav et.al</a></td></code>
                <td>abstractive,question</td>
                <td>fine-tuning</td>
                <td>BERT,ProphetNet</td>
                <td>supervised</td>
                <td>MeQSum</td>
<tr>
        <td><code><a href='https://arxiv.org/pdf/2106.00219.pdf'>S. Yadav et.al</a></td></code>
                <td>abstractive,question</td>
                <td>adaption+fine-tuning</td>
                <td><a href="https://proceedings.neurips.cc/paper/2020/hash/3f5ee243547dee91fbd053c1c4a845aa-Abstract.html">Minilm</a></td>
                <td>supervised</td>
                <td>MeQSum</td>
<tr>
        <td><code><a href='https://aclanthology.org/2021.acl-long.119.pdf'> K. Mrini et.al</a></code> <a href="https://github.com/KhalilMrini/">[code]</a></td> 
                <td>abstractive,question</td>
                <td>adaption+fine-tuning</td>
                <td>BART,BioBERT</td>
                <td>supervised</td>
                <td>MeQSum</td>

        
</tbody >
</table>
"-" in Dataset stands for "not accessible"
</div>



## Evaluation
### Common metrics
[ROUGE](https://aclanthology.org/W04-1013.pdf): 

* ROUGE-N: N-gram overlap between generated summaries of summarizers and gold summaries(relevancy)
* ROUGE-L: the longest common subsequences between generated summaries of summarizers and gold summaries(fluency)

[BertScore](https://arxiv.org/pdf/1904.09675)

### Factual Consistency

Automatic:

* [CheXbert](https://aclanthology.org/2020.emnlp-main.117/) check binary presence values of disease variables
* [Jensen-Shannon Distance](https://github.com/allenai/ms2/) check directions(increase, decrease, no change)

Human Involved

* [Facts Counting](https://arxiv.org/pdf/2104.04412.pdf) 
* [Correctness of PICO and direction](https://aclanthology.org/2022.acl-long.350/)

## Leading Board
### Pubmed

<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th>Model</th>
    <th>ROUGE-1</th>
    <th>ROUGE-2</th>
    <th>ROUGE-L</th>
    <th>Paper</th>
    <th>Code Like</th>
    <th>Source</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> Top Down Transformer(AdaPool)                     </td></code>
		<td> 51.05       </td>
		<td> 23.26    </td>
		<td> 46.47 </td>
		<td> Long Document Summarization with Top-down and Bottom-up Inference (https://arxiv.org/pdf/2203.07586v1.pdf) </td>
		<td> https://github.com/kangbrilliant/DCA-Net      </td>
		<td>arxiv</td>
</tr>
<tr>
	<td><code> LongT5                   </td></code>
		<td> 50.23       </td>
		<td> 24.76    </td>
		<td> 46.67 </td>
		<td> LongT5: Efficient Text-To-Text Transformer for Long Sequences (https://arxiv.org/pdf/2112.07916v2.pdf) </td>
		<td> https://github.com/google-research/longt5      </td>
		<td>NAACL</td>
</tr>
<tr>
	<td><code>MemSum (extractive)                   </td></code>
		<td> 49.25	       </td>
		<td> 22.94    </td>
		<td> 44.42 </td>
		<td> MemSum: Extractive Summarization of Long Documents Using Multi-Step Episodic Markov Decision Processes(https://arxiv.org/pdf/2107.08929v2.pdf) </td>
		<td> https://github.com/nianlonggu/memsum     </td>
		<td>ACL</td>
</tr>
<tr>
	<td><code> HAT-BART                 </td></code>
		<td> 48.25       </td>
		<td> 21.35 </td>
		<td> 36.69 </td>
		<td> Hierarchical Learning for Generation with Long Source Sequences(https://arxiv.org/pdf/2104.07545v2.pdf) </td>
		<td>      </td>
		<td>arxiv</td>
</tr>
<tr>
	<td><code> 	DeepPyramidion                    </td></code>
		<td> 47.81       </td>
		<td> 21.14    </td>
		<td> 46.47 </td>
		<td> Sparsifying Transformer Models with Trainable Representation Pooling
(https://aclanthology.org/2022.acl-long.590.pdf) </td>
		<td> https://github.com/applicaai/pyramidions      </td>
		<td><acl/td>
</tr>
<tr>
	<td><code> 	HiStruct+                   </td></code>
		<td> 46.59       </td>
		<td> 20.39    </td>
		<td> 42.11 </td>
		<td> HiStruct+: Improving Extractive Text Summarization with Hierarchical Structure Information(https://aclanthology.org/2022.findings-acl.102.pdf) </td>
		<td>       </td>
		<td>acl</td>
</tr>
<tr>
	<td><code> DANCER PEGASUS                    </td></code>
		<td> 46.34       </td>
		<td> 19.97    </td>
		<td> 42.42 </td>
		<td> A Divide-and-Conquer Approach to the Summarization of Long Documents[[pdf]](https://arxiv.org/pdf/2004.06190v3.pdf) </td>
		<td> https://github.com/AlexGidiotis/DANCER-summ      </td>
		<td>IEEE/ACM Transactions on Audio Speech and Language Processing</td>
</tr>
<tr>
	<td><code> 	BigBird-Pegasus                     </td></code>
		<td> 46.32       </td>
		<td> 20.65    </td>
		<td> 42.33 </td>
		<td> Big Bird: Transformers for Longer Sequences(https://arxiv.org/pdf/2007.14062v2.pdf) </td>
		<td> https://github.com/google-research/bigbird      </td>
		<td>NeuralIPS</td>
</tr>
<tr>
	<td><code> ExtSum-LG+MMR-Select+                    </td></code>
		<td> 45.39       </td>
		<td> 20.37    </td>
		<td> 40.99 </td>
		<td> Systematically Exploring Redundancy Reduction in Summarizing Long Documents(https://arxiv.org/pdf/2012.00052v1.pdf) </td>
		<td> https://github.com/Wendy-Xiao/redundancy_reduction_longdoc     </td>
		<td>AACL</td>
</tr>
<tr>
	<td><code> 	ExtSum-LG+RdLoss                 </td></code>
		<td> 45.3       </td>
		<td> 20.42    </td>
		<td> 40.95 </td>
		<td> Systematically Exploring Redundancy Reduction in Summarizing Long Documents(https://arxiv.org/pdf/2012.00052v1.pdf) </td>
		<td> https://github.com/Wendy-Xiao/redundancy_reduction_longdoc     </td>
		<td>AACL</td>
</tr>
</tbody >
</table>
</div>



<!--
### Abstractive

1. **Attend to Medical Ontologies: Content Selection for Clinical Abstractive Summarization** `ACL2020` [[pdf]](https://aclanthology.org/2020.acl-main.172.pdf)
2. **Graph enhanced contrastive learning for radiology findings summarization** `ACL2022` [[pdf]](https://aclanthology.org/2022.acl-long.320.pdf)
3. **Covidsum: A linguistically enriched scibert-based summarization model for covid-19 scientific papers**  `Journal of Biomedical
Informatics` [[html]](https://pubmed.ncbi.nlm.nih.gov/35104642/) 
4. **Abstractive summarization of hospitalisation histories with transformer**  `arxiv` [[pdf]](https://arxiv.org/pdf/2204.02208.pdf) 
5. **MNLP at MEDIQA 2021: Fine-Tuning PEGASUS for Consumer Health Question Summarization** `ACL 2021 BioNLP` [[pdf]](https://aclanthology.org/2021.bionlp-1.37.pdf)
6. **paht_nlp @ MEDIQA 2021: Multi-grained Query Focused Multi-Answer Summarization** `NAACL BioNLP 2021` [[pdf]](https://aclanthology.org/2021.bionlp-1.10.pdf)
7. **Optum at MEDIQA 2021: Abstractive Summarization of Radiology Reports using simple BART Finetuning** `NAACL BioNLP 2021` [[pdf]](https://aclanthology.org/2021.bionlp-1.32.pdf)
8. **BDKG at MEDIQA 2021: System Report for the Radiology Report Summarization Task** `NAACL BioNLP 2021` [[pdf]](https://aclanthology.org/2021.bionlp-1.11.pdf)
9. **IBMResearch at MEDIQA 2021: Toward Improving Factual Correctness of Radiology Report Abstractive Summarization** `NAACL BioNLP 2021` [[pdf]](https://aclanthology.org/2021.bionlp-1.35.pdf)
10. **damo_nlp at MEDIQA 2021: Knowledge-based Preprocessing and Coverage-oriented Reranking for Medical Question Summarization** `NAACL BioNLP 2021` [[pdf]](https://aclanthology.org/2021.bionlp-1.12.pdf)
11. **COVID-19 information retrieval with deep-learning based semantic search, question answering, and abstractive summarization** `NPJ digital medicine` [[html]](https://www.nature.com/articles/s41746-021-00437-0)
12. **Msˆ2: Multi-document summarization of medical studie** `EMNLP 2021` [[pdf]](https://aclanthology.org/2021.emnlp-main.594.pdf)
13. **Generating (factual?) narrative summaries of rcts: Experiments with neural multi-document summarization** `AMIA Summits on Translational Science Proceedings` [[html]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8378607/)
14. **Medically Aware GPT-3 as a Data Generator for Medical Dialogue Summarization** `NAACL NLPMC 2021` [[pdf]](https://aclanthology.org/2021.nlpmc-1.9.pdf)
15. **Leveraging Pretrained Models for Automatic Summarization of Doctor-Patient Conversations** `EMNLP findings` [[pdf]](https://aclanthology.org/2021.findings-emnlp.313.pdf)
16. **Generating SOAP Notes from Doctor-Patient Conversations Using Modular Summarization Techniques** `ACL 2021` [[pdf]](https://aclanthology.org/2021.acl-long.384.pdf)
17. **Few-shot fine-tuning SOTA summarization models for medical dialogues** `NAACL 2022` [[pdf]](https://aclanthology.org/2022.naacl-srw.32.pdf)
18. **Biobart: Pretraining and evaluation of a biomedical generative language model** `ACL BioNLP` [[pdf]](https://aclanthology.org/2022.bionlp-1.9.pdf)
19. **Reinforcement Learning for Abstractive Question Summarization with Question-aware Semantic Rewards** `ACL 2021` [[pdf]](https://aclanthology.org/2021.acl-short.33.pdf)
20. **Question-aware transformer models for consumer health question summarization** `Journal of Biomedical Informatics` [[pdf]](https://arxiv.org/pdf/2106.00219.pdf)
21. **A Gradually Soft Multi-Task and Data-Augmented Approach to Medical Question Understanding** `ACL 2021` [[pdf]](https://aclanthology.org/2021.acl-long.119.pdf)
22.

### Extractive Model

1. **** `` [[]]()
2. **** `` [[]]()
3. **** `` [[]]()
4. **** `` [[]]()
5. 	**** `` [[]]()

### Joint Model

1. **A Co-Interactive Transformer for Joint Slot Filling and Intent Detection**(ATIS/SNIPS) `ICASSP 2021` [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) [[code]](https://github.com/kangbrilliant/DCA-Net)
2. **SlotRefine: A Fast Non-Autoregressive Model for Joint Intent Detection and Slot Filling** (ATIS/SNIPS) `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.emnlp-main.152.pdf) [[code]](https://github.com/moore3930/SlotRefine)
3. **Joint Slot Filling and Intent  Detection via Capsule Neural Networks** (ATIS/SNIPS) `ACL 2019` [[pdf]](https://arxiv.org/pdf/1812.09471.pdf) [[code]](https://github.com/czhang99/Capsule-NLU) 
4. **BERT for Joint Intent  Classification and Slot Filling** (ATIS/SNIPS/Stanford Dialogue Dataset) `arXiv 2019` [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) [[code]](https://github.com/monologg/JointBERT) 
5. **A Novel Bi-directional  Interrelated Model for Joint Intent Detection and Slot Filling** (ATIS/Stanford Dialogue Dataset/SNIPS) `ACL 2019` [[pdf]](https://www.aclweb.org/anthology/P19-1544.pdf) [[code]](https://github.com/ZephyrChenzf/SF-ID-Network-For-NLU) 
6. **CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding** (ATIS/SNIPS/CAIS) `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf) [[code]](https://github.com/Adaxry/CM-Net) 
7. **Slot-Gated Modeling for Joint  Slot Filling and Intent Prediction** (ATIS/Stanford Dialogue Dataset,SNIPS) `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-2118.pdf) [[code]](https://github.com/MiuLab/SlotGated-SLU) 
8. **Joint Online Spoken Language  Understanding and Language Modeling with Recurrent Neural Networks** (ATIS) `SIGDIAL 2016` [[pdf]](https://www.aclweb.org/anthology/W16-3603.pdf) [[code]](https://github.com/HadoopIt/joint-slu-lm)

### Complex SLU Model

1. **How Time Matters: Learning Time-Decay Attention for Contextual Spoken Language Understanding in Dialogues** (DSTC4) `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1194.pdf) [[code]](https://github.com/MiuLab/Time-Decay-SLU) 
2. **Speaker Role Contextual Modeling for Language Understanding and Dialogue Policy Learning** (DSTC4) `IJCNLP 2017` [[pdf]](https://www.aclweb.org/anthology/I17-2028.pdf) [[code]](https://github.com/MiuLab/Spk-Dialogue) 
3. **Dynamic time-aware attention to speaker roles and contexts for spoken language understanding** (DSTC4) `IEEE 2017` [[pdf]](https://arxiv.org/pdf/1710.00165.pdf) [[code]](https://github.com/MiuLab/Time-SLU) 
4. **Injecting Word Information with Multi-Level Word Adapter for Chinese Spoken Language Understanding** (CAIS/ECDT-NLU) `arXiv 2020` [[pdf]](https://arxiv.org/pdf/2010.03903.pdf) [[code]](https://github.com/AaronTengDeChuan/MLWA-Chinese-SLU) 
5. **CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding** (ATIS/SNIPS/CAIS) `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf) [[code]](https://github.com/Adaxry/CM-Net) 
6. **Coach: A Coarse-to-Fine  Approach for Cross-domain Slot Filling** (SNIPS) `ACL 2020` [[pdf]](https://arxiv.org/pdf/2004.11727.pdf) [[code]](https://github.com/zliucr/coach)
7. **CoSDA-ML: Multi-Lingual  Code-Switching Data Augmentation for Zero-Shot Cross-Lingual NLP** (SC2/4/MLDoc/Multi WOZ/Facebook Multilingual SLU Dataset) `IJCAI 2020` [[pdf]](https://arxiv.org/pdf/2006.06402.pdf) [[code]](https://github.com/kodenii/CoSDA-ML) 
8. **Cross-lingual Spoken Language  Understanding with Regularized Representation Alignment** (Multilingual spoken language understanding (SLU) dataset) `EMNLP 2020` [[pdf]](https://arxiv.org/pdf/2009.14510.pdf) [[code]](https://github.com/zliucr/crosslingual-slu.)
9. **Attention-Informed  Mixed-Language Training for Zero-shot Cross-lingual Task-oriented Dialogue  Systems** (Facebook Multilingual SLU Dataset/(DST)MultiWOZ) `AAAI 2020` [[pdf]](https://arxiv.org/pdf/1911.09273.pdf) [[code]](https://github.com/zliucr/mixedlanguage-training) 
10. **MTOP: A Comprehensive Multilingual Task-Oriented Semantic Parsing Benchmark** (MTOP/Multilingual ATIS) `arXiv 2020` [[pdf]](https://arxiv.org/pdf/2008.09335.pdf) [[code]]() 
11. **Neural Architectures for  Multilingual Semantic Parsing** (GEO/ATIS) `ACL 2017` [[pdf]](https://www.aclweb.org/anthology/P17-2007.pdf) [[code]](http://statnlp.org/research/sp/) 
12. **Few-shot Learning for Multi-label Intent Detection** (TourSG/StandfordLU) `AAAI 2021` [[pdf]](https://arxiv.org/abs/2010.05256.pdf) [[code]](https://github.com/AtmaHou/FewShotMultiLabel) 
13. **Few-shot Slot Tagging with Collapsed Dependency Transfer and Label-enhanced Task-adaptive Projection Network** (SNIPS and further construct) `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.128.pdf) [[code]](https://github.com/AtmaHou/FewShotTagging)




## Frontiers

### Single Slot Filling

1. **Few-shot Slot Tagging with  Collapsed Dependency Transfer and Label-enhanced Task-adaptive Projection  Network** (SNIPS) `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.128.pdf) [[code]](https://github.com/AtmaHou/FewShotTagging) 
2. **A Hierarchical Decoding Model  For Spoken Language Understanding From Unaligned Data** (DSTC2) `ICASSP 2019` [[pdf]](https://arxiv.org/pdf/1904.04498.pdf) 
3. **Utterance Generation With  Variational Auto-Encoder for Slot Filling in Spoken Language Understanding** (ATIS/SNIPS/MIT Corpus) `IEEE Signal Processing Letters 2019` [[pdf]]([https://ieeexplore.ieee.org/document/8625384](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8625384)) 
4. **Data Augmentation with Atomic  Templates for Spoken Language Understanding** (ATIS) `EMNLP 2019` [[pdf]](https://arxiv.org/pdf/1908.10770.pdf) 
5. **A New Concept of Deep  Reinforcement Learning based Augmented General Sequence Tagging System** (ATIS/CNLL-2003) `COLING 2018` [[pdf]](https://www.aclweb.org/anthology/C18-1143.pdf) 
6. **Improving Slot Filling in  Spoken Language Understanding with Joint Pointer and Attention** (DSTC2) `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-2068.pdf) 
7. **Sequence-to-Sequence Data  Augmentation for Dialogue Language Understanding** (ATIS/Stanford Dialogue Dataset) `COLING 2018` [[pdf]](https://arxiv.org/pdf/1807.01554.pdf) [[code]](https://github.com/AtmaHou/Seq2SeqDataAugmentationForLU) 
8. **Encoder-Decoder with  Focus-Mechanism for Sequence Labelling Based Spoken Language Understanding** (ATIS) `ICASSP 2017` [[pdf]]([https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=79532433](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7953243)) 
9. **Neural Models for Sequence  Chunking** (ATIS/LARGE) `AAAI 2017` [[pdf]](https://arxiv.org/pdf/1701.04027.pdf) 
10. **Bi-directional recurrent  neural network with ranking loss for spoken language understanding** (ATIS) `IEEE 2016` [[pdf]](https://ieeexplore.ieee.org/abstract/document/7472841/) 
11. **Labeled Data Generation with  Encoder-decoder LSTM for Semantic Slot Filling** (ATIS) `INTERSPEECH 2016` [[pdf]](https://pdfs.semanticscholar.org/7ffe/83d7dd3a474e15ccc2aef412009f100a5802.pdf) 
12. **Syntax or Semantics?  Knowledge-Guided Joint Semantic Frame Parsing** (ATIS/Cortana) `IEEE Workshop on Spoken Language Technology 2016` [[pdf]](https://www.csie.ntu.edu.tw/~yvchen/doc/SLT16_SyntaxSemantics.pdf) 
13. **Bi-Directional Recurrent  Neural Network with Ranking Loss for Spoken Language Understanding** (ATIS) `ICASSP 2016` [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7472841) 
14. **Leveraging Sentence-level  Information with Encoder LSTM for Semantic Slot Filling** (ATIS) `EMNLP 2016` [[pdf]](https://www.aclweb.org/anthology/D16-1223.pdf) 
15. **Labeled Data Generation with  Encoder-decoder LSTM for Semantic Slot Filling** (ATIS) `INTERSPEECH 2016` [[pdf]](https://www.isca-speech.org/archive/Interspeech_2016/pdfs/0727.PDF) 
16. **Using Recurrent Neural  Networks for Slot Filling in Spoken Language Understanding** (ATIS) `IEEE/ACM TASLP 2015` [[pdf]](https://ieeexplore.ieee.org/document/6998838) 
17. **Using Recurrent Neural  Networks for Slot Filling in Spoken Language Understanding** (ATIS) `IEEE/ACM Transactions on Audio, Speech, and Language  Processing 2015` [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6998838) 
18. **Recurrent  Neural Network Structured Output Prediction for Spoken Language Understanding** (ATIS) `- 2015` [[pdf]](http://speech.sv.cmu.edu/publications/liu-nipsslu-2015.pdf) 
19. **Spoken Language Understanding  Using Long Short-Term Memory Neural Networks** (ATIS) `IEEE 2014` [[pdf]](https://groups.csail.mit.edu/sls/publications/2014/Zhang_SLT_2014.pdf) 
20. **Recurrent conditional random  field for language understanding** (ATIS) `IEEE 2014` [[pdf]](https://ieeexplore.ieee.org/document/6854368) 
21. **Recurrent Neural Networks for  Language Understanding** (ATIS) `INTERSPEECH 2013` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/kaisheny-338_file_paper.pdf) 
22. **Investigation of  Recurrent-Neural-Network Architectures and Learning Methods for Spoken  Language Understanding** (ATIS) `ISCA 2013` [[pdf]](https://www.isca-speech.org/archive/archive_papers/interspeech_2013/i13_3771.pdf) 
23. **Large-scale personal assistant  technology deployment: the siri experience** (-) `INTERSPEECH 2013` [[pdf]](https://isca-speech.org/archive/archive_papers/interspeech_2013/i13_2029.pdf) 

### Single Intent Detection

1. **Zero-shot User Intent  Detection via Capsule Neural Networks** (SNIPS/CVA) `EMNLP 2018` [[pdf]](https://arxiv.org/pdf/1809.00385.pdf) 
2. **Intention Detection Based on Siamese Neural Network With Triplet Loss** (SNIPS/ATIS/Facebook multilingual datasets/ Daily Dialogue/MRDA) `IEEE Acess 2020` [[pdf]](https://ieeexplore.ieee.org/document/9082602) 
3. **Multi-Layer Ensembling Techniques for Multilingual Intent Classification** (ATIS) `arXiv 2018` [[pdf]](https://arxiv.org/pdf/1806.07914.pdf) 
4. **Deep Unknown Intent Detection with Margin Loss** (SNIPS/ATIS) `ACL 2019` [[pdf]](https://arxiv.org/pdf/1906.00434.pdf) 
5. **Subword Semantic Hashing for Intent Classification on Small Datasets** (The Chatbot Corpus/The AskUbuntu Corpus) `IJCNN 2019` [[pdf]](https://arxiv.org/pdf/1810.07150.pdf) 
6. **Dialogue intent classification with character-CNN-BGRU networks** (the Chinese Wikipedia dataset) `Multimedia Tools and Applications 2018` [[pdf]](https://link.springer.com/article/10.1007/s11042-019-7678-1)  
7. **Joint Learning of Domain Classification and Out-of-Domain Detection with Dynamic Class Weighting for Satisficing False Acceptance Rates** (Alexa) `InterSpeech 2018` [[pdf]](https://www.isca-speech.org/archive/Interspeech_2018/pdfs/1581.pdf)  
8. **Recurrent neural network and  LSTM models for lexical utterance classification** (ATIS/CB) `INTERSPEECH 2015` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/RNNLM_addressee.pdf) 
9. **Adversarial Training for Multi-task and Multi-lingual Joint Modeling of Utterance Intent Classification** (collected by the author) `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1064.pdf) 
10. **Exploiting Shared Information for Multi-Intent Natural Language Sentence Classification** (collected by the author) `ISCA 2013` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2013/08/double_intent.pdf)  

### Joint Model

#### Implicit joint modeling

1.  **Leveraging Non-Conversational  Tasks for Low Resource Slot Filling: Does it help?** (ATIS/MIT Restaurant, and Movie/OntoNotes 5.0/OPUS   News Commentary) `SIGDIAL 2019` [[pdf]](https://www.aclweb.org/anthology/W19-5911.pdf) 
2.  **Simple, Fast, Accurate Intent Classification and Slot Labeling for Goal-Oriented Dialogue Systems** (ATIS/SNIPS) `SIGDIAL 2019` [[pdf]](https://www.aclweb.org/anthology/W19-5906.pdf)
3.  **Multi-task learning for Joint  Language Understanding and Dialogue State Tracking** (M2M/DSTC2) `SIGDIAL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-5045.pdf) 
4.  **A Joint Model of Intent  Determination and Slot Filling for Spoken Language Understanding** (ATIS/CQUD) `IJCAI 2016` [[pdf]](https://www.ijcai.org/Proceedings/16/Papers/425.pdf) 
5.  **Joint Online Spoken Language  Understanding and Language Modeling with Recurrent Neural Networks** (ATIS) `SIGDIAL 2016` [[pdf]](https://www.aclweb.org/anthology/W16-3603.pdf) [[code]](https://github.com/HadoopIt/joint-slu-lm)
6.  **Multi-Domain Joint Semantic  Frame Parsing using Bi-directional RNN-LSTM** (ATIS) `INTERSPEECH 2016` [[pdf]](https://pdfs.semanticscholar.org/d644/ae996755c803e067899bdd5ea52498d7091d.pdf) 
7.  **Attention-Based Recurrent  Neural Network Models for Joint Intent Detection and Slot Filling** (ATIS) `INTERSPEECH 2016` [[pdf]](https://arxiv.org/pdf/1609.01454.pdf) 
8.  **Multi-domain joint semantic  frame parsing using bi-directional RNN-LSTM** (ATIS) `INTERSPEECH 2016` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/06/IS16_MultiJoint.pdf) 
9.  **JOINT SEMANTIC UTTERANCE  CLASSIFICATION AND SLOT FILLING WITH RECURSIVE NEURAL NETWORKS** (ATIS/Stanford Dialogue Dataset,Microsoft Cortana  conversational understanding task(-)) `IEEE SLT 2014` [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7078634) 
10.  **CONVOLUTIONAL NEURAL NETWORK  BASED TRIANGULAR CRF FOR JOINT INTENT DETECTION AND SLOT FILLING** (ATIS) `IEEE Workshop on Automatic Speech Recognition and  Understanding 2013` [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6707709) 

#### Explicit joint modelling

1.	**A Result based Portable Framework for Spoken Language Understanding**(KVRET) `ICME 2021` [[pdf]](https://arxiv.org/pdf/2103.06010.pdf) 
2.  **A Co-Interactive Transformer for Joint Slot Filling and Intent Detection**(ATIS/SNIPS) `ICASSP 2021` [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) [[code]](https://github.com/kangbrilliant/DCA-Net)
3.  **SlotRefine: A Fast Non-Autoregressive Model for Joint Intent Detection and Slot Filling** (ATIS/SNIPS) `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.emnlp-main.152.pdf) [[code]](https://github.com/moore3930/SlotRefine)
4.  **Graph LSTM with Context-Gated Mechanism for Spoken Language Understanding**(ATIS/SNIPS) `AAAI 2020` [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/6499/6355) 
5.  **Joint Slot Filling and Intent  Detection via Capsule Neural Networks** (ATIS/SNIPS) `ACL 2019` [[pdf]](https://arxiv.org/pdf/1812.09471.pdf) [[code]](https://github.com/czhang99/Capsule-NLU) 
6.  **A Stack-Propagation Framework  with Token-Level Intent Detection for Spoken Language Understanding** (ATIS/SNIPS) `EMNLP 2019` [[pdf]](https://arxiv.org/pdf/1909.02188.pdf) [[code]](https://github.com/LeePleased/StackPropagation-SLU) 
7.  **A Joint Learning Framework  With BERT for Spoken Language Understanding** (ATIS/SNIPS/Facebook's Multilingual dataset) `IEEE 2019` [[pdf]](https://ieeexplore.ieee.org/document/8907842) 
8.  **BERT for Joint Intent  Classification and Slot Filling** (ATIS/SNIPS/Stanford Dialogue Dataset) `arXiv 2019` [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) [[code]](https://github.com/monologg/JointBERT) 
9.  **A Novel Bi-directional  Interrelated Model for Joint Intent Detection and Slot Filling** (ATIS/Stanford Dialogue Dataset,SNIPS) `ACL 2019` [[pdf]](https://www.aclweb.org/anthology/P19-1544.pdf) [[code]](https://github.com/ZephyrChenzf/SF-ID-Network-For-NLU) 
10.  **Joint Multiple Intent  Detection and Slot Labeling for Goal-Oriented Dialog** (ATIS/Stanford Dialogue Dataset/SNIPS) `NAACL 2019` [[pdf]](https://www.aclweb.org/anthology/N19-1055.pdf) 
11.  **CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding** (ATIS/SNIPS/CAIS) `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf) [[code]](https://github.com/Adaxry/CM-Net) 
12.  **A Bi-model based RNN Semantic  Frame Parsing Model for Intent Detection and Slot Filling** (ATIS) `NAACL 2018` [[pdf]](https://arxiv.org/pdf/1812.10235.pdf) 
13.  **Slot-Gated Modeling for Joint  Slot Filling and Intent Prediction** (ATIS/Stanford Dialogue Dataset,SNIPS) `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-2118.pdf) [[code]](https://github.com/MiuLab/SlotGated-SLU) 
14.  **A Self-Attentive Model with  Gate Mechanism for Spoken Language Understanding** (ATIS) `EMNLP 2018` [[pdf]](https://www.aclweb.org/anthology/D18-1417.pdf) 

### Contextual SLU

2. **Knowing Where to Leverage: Context-Aware Graph Convolutional Network with An Adaptive Fusion Layer for Contextual Spoken Language Understanding** (Simulated Dialogues dataset) `IEEE 2021` [[pdf]](https://ieeexplore.ieee.org/document/9330801) 
2. **Dynamically Context-sensitive Time-decay Attention for Dialogue Modeling** (DSTC4) `IEEE 2019` [[pdf]](https://arxiv.org/pdf/1809.01557.pdf) 
3. **Multi-turn Intent Determination for Goal-oriented Dialogue systems** (Frames/Key-Value Retrieval) `IJCNN 2019` [[pdf]](https://ieeexplore.ieee.org/document/8852246) 
4. **Transfer Learning for Context-Aware Spoken Language Understanding** (single-turn: ATIS/SNIPS multi-turn: Simulated Dialogues dataset) `IEEE 2019` [[pdf]](https://ieeexplore.ieee.org/document/9003902) 
5. **How Time Matters: Learning Time-Decay Attention for Contextual Spoken Language Understanding in Dialogues** (DSTC4) `NAACL 2018` [[pdf]](https://www.aclweb.org/anthology/N18-1194.pdf) [[code]](https://github.com/MiuLab/Time-Decay-SLU) 
6. **An Efficient Approach to Encoding Context for Spoken Language Understanding** (Simulated Dialogues dataset) `InterSpeech 2018` [[pdf]](https://arxiv.org/pdf/1807.00267.pdf) 
7. **Speaker-sensitive dual memory networks for multi-turn slot tagging** (Microsoft Cortana) `IEEE 2017` [[pdf]](https://arxiv.org/pdf/1711.10705.pdf) 
8. **Speaker Role Contextual Modeling for Language Understanding and Dialogue Policy Learning** (DSTC4) `IJCNLP 2017` [[pdf]](https://www.aclweb.org/anthology/I17-2028.pdf) [[code]](https://github.com/MiuLab/Spk-Dialogue) 
9. **Sequential dialogue context modeling for spoken language understanding** (collected by the author) `SIGDIAL 2017` [[pdf]](https://arxiv.org/pdf/1705.03455.pdf) 
10. **End-to-end joint learning of natural language understanding and dialogue manager** (DSTC4) `IEEE 2017` [[pdf]](https://arxiv.org/pdf/1612.00913.pdf) [[code]](https://github.com/XuesongYang/end2end_dialog.git) 
11. **Dynamic time-aware attention to speaker roles and contexts for spoken language understanding** (DSTC4) `IEEE 2017` [[pdf]](https://arxiv.org/pdf/1710.00165.pdf) [[code]](https://github.com/MiuLab/Time-SLU) 
12. **An Intelligent Assistant for High-Level Task Understanding** (collected by the author) `IUI 2016` [[pdf]](http://www.cs.cmu.edu/~mings/papers/IUI16IntelligentAssistant.pdf) 
13. **End-to-End Memory Networks with Knowledge Carryover for Multi-Turn Spoken Language Understanding** (Collected from Microsoft Cortana) `INTEERSPEECH 2016` [[pdf]](https://pdfs.semanticscholar.org/df07/45ce821007cb3122f00509cc18f2885fa8bd.pdf) 
14. **Leveraging behavioral patterns of mobile applications for personalized spoken language understanding** (collected by the author) `ICMI 2015` [[pdf]](https://www.csie.ntu.edu.tw/~yvchen/doc/ICMI15_MultiModel.pdf) 
15. **Contextual spoken language understanding using recurrent neural networks** (single-turn: ATIS multi-turn: Microsoft Cortana) ` 2015` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/0005271.pdf) 
16. **Contextual domain classification in spoken language understanding systems using recurrent neural network** (collected by the author) `IEEE 2014` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2014/05/rnn_dom.pdf) 
17. **Easy contextual intent prediction and slot detection** (collected by the author) `IEEE 2013` [[pdf]](https://ieeexplore.ieee.org/document/6639291) 

### Multi-intent SLU

1. **AGIF: An Adaptive Graph-Interactive Framework for Joint Multiple Intent Detection and Slot Filling** (MixATIS/MixSNIPS) `EMNLP 2020` [[pdf]](https://www.aclweb.org/anthology/2020.findings-emnlp.163.pdf) [[code]](https://github.com/LooperXX/AGIF)
2. **Joint Multiple Intent Detection and Slot Labeling for Goal-Oriented Dialog** (ATIS/SNIPS/internal dataset) `NACCL 2019` [[pdf]](https://www.aclweb.org/anthology/N19-1055.pdf)
3. **Two-stage multi-intent detection for spoken language understanding** (Korean-language corpus for the TV guide domain colleted by author) `Multimed Tools Appl 2017` [[pdf]](https://link.springer.com/article/10.1007/s11042-016-3724-4)
4. **Exploiting Shared Information for Multi-intent Natural Language Sentence Classification** (inhouse corpus from Microsoft) `Interspeech 2013` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2013/08/double_intent.pdf)

### Chinese SLU

1. **Injecting Word Information with Multi-Level Word Adapter for Chinese Spoken Language Understanding** (CAIS/ECDT-NLU) `arXiv 2020` [[pdf]](https://arxiv.org/pdf/2010.03903.pdf) [[code]](https://github.com/AaronTengDeChuan/MLWA-Chinese-SLU) 
2. **CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding** (ATIS/SNIPS/CAIS) `EMNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf) [[code]](https://github.com/Adaxry/CM-Net) 

### Cross-domain SLU

1. **Coach: A Coarse-to-Fine  Approach for Cross-domain Slot Filling** (SNIPS) `ACL 2020` [[pdf]](https://arxiv.org/pdf/2004.11727.pdf) [[code]](https://github.com/zliucr/coach)
2. **Towards  Scalable Multi-Domain Conversational Agents: The Schema-Guided Dialogue  Dataset** (SGD) `AAAI 2020` [[pdf]](https://arxiv.org/pdf/1909.05855.pdf) 
3. **Unsupervised Transfer Learning  for Spoken Language Understanding in Intelligent Agents** (ATIS/SINPS) `AAAI 2019` [[pdf]](https://arxiv.org/pdf/1811.05370.pdf) 
4. **Zero-Shot Adaptive Transfer  for Conversational Language Understanding** (collected by author) `AAAI 2019` [[pdf]](https://arxiv.org/pdf/1808.10059.pdf) 
5. **Robust Zero-Shot Cross-Domain  Slot Filling with Example Values** (SNIPS/XSchema) `ACL 2019` [[pdf]](https://arxiv.org/pdf/1906.06870.pdf) 
6. **Concept Transfer Learning for  Adaptive Language Understanding** (ATIS/DSTC2&3) `SIGDIAL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-5047.pdf) 
7. **Fast and Scalable Expansion of  Natural Language Understanding Functionality for Intelligent Agents** (generated by the author) `NAACL 2018` [[pdf]](https://arxiv.org/pdf/1805.01542.pdf) 
8. **Bag of Experts Architectures  for Model Reuse in Conversational Language Understanding** (generated by the author) `NAACL-HLT 2018` [[pdf]](https://www.aclweb.org/anthology/N18-3019.pdf) 
9. **Domain Attention with an  Ensemble of Experts** (corpus 7 Microsoft Cortana domains) `ACL 2017` [[pdf]](https://www.aclweb.org/anthology/P17-1060.pdf) 
10. **Towards Zero-Shot Frame  Semantic Parsing for Domain Scaling** `INTERSPEECH 2017` (collected by the author) [[pdf]](https://arxiv.org/pdf/1707.02363.pdf) 
11. **Zero-Shot Learning across  Heterogeneous Overlapping Domains** `INTERSPEECH 2017` (inhouse data from Amazon) [[pdf]](https://www.isca-speech.org/archive/Interspeech_2017/pdfs/0516.PDFF) 
12. **Domainless Adaptation by  Constrained Decoding on a Schema Lattice** (Cortana) `COLING 2016` [[pdf]](https://www.aclweb.org/anthology/C16-1193.pdf) 
13. **Domain Adaptation of Recurrent  Neural Networks for Natural Language Understanding** (United Airlines/Airbnb/Grey-hound bus service/OpenTable (Data  obtained from App)) `INTERSPEECH 2016` [[pdf]](https://arxiv.org/pdf/1604.00117.pdf) 
14. **Natural Language Model  Re-usability for Scaling to Different Domains** (ATIS/MultiATIS) `EMNLP 2016` [[pdf]](https://www.aclweb.org/anthology/D16-1222.pdf) 
15. **Frustratingly Easy Neural  Domain Adaptation** (Cortana) `COLING 2016` [[pdf]](https://www.aclweb.org/anthology/C16-1038.pdf) 
16. **Multi-Domain Joint Semantic  Frame Parsing using Bi-directional RNN-LSTM** (ATIS) `INTERSPEECH 2016` [[pdf]](https://pdfs.semanticscholar.org/d644/ae996755c803e067899bdd5ea52498d7091d.pdf) 
17. **A Model of Zero-Shot Learning  of Spoken Language Understanding** (generated by the author) `EMNLP 2015` [[pdf]](https://www.aclweb.org/anthology/D15-1027.pdf) 
18. **Online adaptative zero-shot learning spoken language understanding using word-embedding** (DSTC2) `IEEE 2015` [[pdf]](https://ieeexplore.ieee.org/document/7178987) 
19. **Multi-Task Learning for Spoken  Language Understanding with Shared Slots** (collected by the author) `INTERSPEECH 2011` [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2011/08/Xiao-IS11.pdf) 

### Cross-lingual SLU

1. **CoSDA-ML: Multi-Lingual  Code-Switching Data Augmentation for Zero-Shot Cross-Lingual NLP** (SC2/4/MLDoc/Multi WOZ/Facebook Multilingual SLU Dataset) `IJCAI 2020` [[pdf]](https://arxiv.org/pdf/2006.06402.pdf) [[code]](https://github.com/kodenii/CoSDA-ML) 
2. **Cross-lingual Spoken Language  Understanding with Regularized Representation Alignment** (Multilingual spoken language understanding (SLU) dataset) `EMNLP 2020` [[pdf]](https://arxiv.org/pdf/2009.14510.pdf) [[code]](https://github.com/zliucr/crosslingual-slu.) 
3. **End-to-End Slot Alignment and  Recognition for Cross-Lingual NLU** (ATIS/MultiATIS) `EMNLP 2020` [[pdf]](https://arxiv.org/pdf/2004.14353.pdf) 
4. **Multi-Level Cross-Lingual  Transfer Learning With Language Shared and Specific Knowledge for Spoken  Language Understanding** (Facebook Multilingual SLU Dataset) `IEEE Access 2020` [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8990095) 
5. **Attention-Informed  Mixed-Language Training for Zero-shot Cross-lingual Task-oriented Dialogue  Systems** (Facebook Multilingual SLU Dataset/(DST)MultiWOZ) `AAAI 2020` [[pdf]](https://arxiv.org/pdf/1911.09273.pdf) [[code]](https://github.com/zliucr/mixedlanguage-training) 
6. **MTOP: A Comprehensive Multilingual Task-Oriented Semantic Parsing Benchmark** (MTOP /Multilingual ATIS) `arXiv 2020` [[pdf]](https://arxiv.org/pdf/2008.09335.pdf) [[code]]() 
7. **Cross-lingual Transfer  Learning with Data Selection for Large-Scale Spoken Language Understanding** (ATIS) `EMNLP-IJCNLP 2019` [[pdf]](https://www.aclweb.org/anthology/D19-1153.pdf) 
8. **Zero-shot Cross-lingual  Dialogue Systems with Transferable Latent Variables** (Facebook Multilingual SLU Dataset) `EMNLP-IJCNLP 2019` [[pdf]](https://arxiv.org/pdf/1911.04081.pdf) 
9. **Cross-Lingual Transfer  Learning for Multilingual Task Oriented Dialog** (Facebook Multilingual SLU Dataset) `NAACL 2019` [[pdf]](https://arxiv.org/pdf/1810.13327.pdf) 
10. **Almawave-SLU: A new dataset  for SLU in Italian** (Valentina.Bellomaria@almawave.it) `CEUR Workshop 2019` [[pdf]](https://arxiv.org/pdf/1907.07526.pdf) 
11. **Multi-lingual Intent Detection  and Slot Filling in a Joint BERT-based Model** (ATIS/SNIPS) `arXiv 2019` [[pdf]](https://arxiv.org/pdf/1907.02884.pdf) 
12. **(Almost) Zero-Shot  Cross-Lingual Spoken Language Understanding** (ATIS manually translated into Hindi and Turkish) `IEEE/ICASSP 2018` [[pdf]](http://shyamupa.com/papers/UFTHH18.pdf) 
14. **Neural Architectures for  Multilingual Semantic Parsing** (GEO/ATIS) `ACL 2017` [[pdf]](https://www.aclweb.org/anthology/P17-2007.pdf) [[code]](http://statnlp.org/research/sp/) 
15. **Multi-style adaptive training  for robust cross-lingual spoken language understanding** (English-Chinese ATIS) `IEEE 2013` [[pdf]](https://ieeexplore.ieee.org/abstract/document/6639292) 
16. **ASGARD: A PORTABLE  ARCHITECTURE FOR MULTILINGUAL DIALOGUE SYSTEMS** (collected from crowd-sourcing platform) `ICASSP 2013` [[pdf]](https://groups.csail.mit.edu/sls/publications/2013/Liu_ICASSP-2013.pdf) 
17. **Combining multiple translation  systems for Spoken Language Understanding portability** (MEDIA) `IEEE 2012` [[pdf]](https://ieeexplore.ieee.org/document/6424221) 

### Low-resource SLU

#### Few-shot SLU

1. **Few-shot Learning for Multi-label Intent Detection** (TourSG/StandfordLU) `AAAI 2021` [[pdf]](https://arxiv.org/abs/2010.05256) [[code]](https://github.com/AtmaHou/FewShotMultiLabel) 
2. **Few-shot Slot Tagging with Collapsed Dependency Transfer and Label-enhanced Task-adaptive Projection Network** (SNIPS and further construct) `ACL 2020` [[pdf]](https://www.aclweb.org/anthology/2020.acl-main.128.pdf) [[code]](https://github.com/AtmaHou/FewShotTagging)
3. **Data Augmentation for Spoken  Language Understanding via Pretrained Models** (ATIS/SNIPS) `arXiv 2020` [[pdf]](https://arxiv.org/pdf/2004.13952.pdf) 
4. **Data augmentation by data  noising for open vocabulary slots in spoken language understanding** (ATIS/Snips/MIT-Restaurant.) `NAACL-HLT 2019` [[pdf]](https://www.aclweb.org/anthology/N19-3014.pdf) 
5. **Data Augmentation for Spoken  Language Understanding via Joint Variational Generation** (ATIS) `AAAI 2019` [[pdf]](https://arxiv.org/pdf/1809.02305.pdf) 
6. **Marrying Up Regular  Expressions with Neural Networks: A Case Study for Spoken Language  Understanding** (ATIS) `ACL 2018` [[pdf]](https://www.aclweb.org/anthology/P18-1194.pdf) 
7. **Concept Transfer Learning for  Adaptive Language Understanding** (ATIS/DSTC2&3) `SIGDIAL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-5047.pdf) 

#### Zero-shot SLU
1. **Coach: A Coarse-to-Fine  Approach for Cross-domain Slot Filling** (SNIPS) `ACL 2020` [[pdf]](https://arxiv.org/pdf/2004.11727.pdf) [[code]](https://github.com/zliucr/coach)
2. **Zero-Shot Adaptive Transfer  for Conversational Language Understanding** (collected by the author) `AAAI 2019` [[pdf]](https://arxiv.org/pdf/1808.10059.pdf) 
3. **Toward zero-shot Entity  Recognition in Task-oriented Conversational Agents** (Entity gazetteers/Synthetic Gazetteers/Synthetic Utterances) `SIGDIAL 2018` [[pdf]](https://www.aclweb.org/anthology/W18-5036.pdf) 
4. **Zero-shot User Intent  Detection via Capsule Neural Networks** (SNIPS/CVA) `EMNLP 2018` [[pdf]](https://arxiv.org/pdf/1809.00385.pdf) 
5. **Towards Zero-Shot Frame  Semantic Parsing for Domain Scaling** `INTERSPEECH 2017` [[pdf]](https://arxiv.org/pdf/1707.02363.pdf) 
6. **Zero-Shot Learning across  Heterogeneous Overlapping Domains** `INTERSPEECH 2017` [[pdf]](https://www.isca-speech.org/archive/Interspeech_2017/pdfs/0516.PDFF) 
7. **A Model of Zero-Shot Learning  of Spoken Language Understanding** (generated by the author) `EMNLP 2015` [[pdf]](https://www.aclweb.org/anthology/D15-1027.pdf) 
8. **Zero-shot semantic parser for  spoken language understanding** (DSTC2&3) `INTERSPEECH 2015` [[pdf]](https://www.isca-speech.org/archive/interspeech_2015/papers/i15_1403.pdf) 

#### Unsupervised SLU

1. **Deep Open Intent Classification with Adaptive Decision Boundary** (Banking-77 / CLINC150) `AAAI 2021`  [[pdf]](https://arxiv.org/pdf/2012.10209.pdf) [[code]](https://github.com/thuiar/Adaptive-Decision-Boundary)
2. **Discovering New Intents with Deep Aligned Clustering** (Banking-77 / CLINC150) `AAAI 2021`  [[pdf]](https://arxiv.org/pdf/2012.08987.pdf) [[code]](https://github.com/thuiar/DeepAligned-Clustering)
3. **Discovering New Intents via Constrained Deep Adaptive Clustering with Cluster Refinement** (SNIPS) `AAAI 2020`  [[pdf]](https://arxiv.org/pdf/1911.08891.pdf) [[code]](https://github.com/thuiar/CDAC-plus)
4. **Dialogue State Induction Using Neural Latent Variable Models** (MultiWOZ 2.1/SGD) `IJCAI 2020`  [[pdf]](https://www.ijcai.org/proceedings/2020/0532.pdf)
-->
<!--
## LeaderBoard
### ATIS

#### Non-pretrained model

<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th> Model</th>
    <th>Intent Acc</th>
    <th>Slot F1</th>
    <th>Paper / Source</th>
    <th>Code link</th>
    <th>Conference</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> Co-Interactive(Qin et al., 2021)                         </td></code>
		<td> 97.7       </td>
		<td> 95.9    </td>
		<td> A Co-Interactive Transformer for Joint Slot Filling and Intent Detection  [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) </td>
		<td> https://github.com/kangbrilliant/DCA-Net      </td>
		<td> ICASSP  </td>
		<td></td>
</tr>
<tr>
	<td><code> Graph LSTM(Zhang et al., 2021)                         </td></code>
		<td> 97.20      </td>
		<td> 95.91    </td>
		<td> Graph LSTM with Context-Gated Mechanism for Spoken Language Understanding  [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/6499/6355) </td>
		<td> -      </td>
		<td> AAAI  </td>
		<td></td>
</tr>
<tr>
	<td><code> Stack  Propagation(Qin et al., 2019)                         </td></code>
		<td> 96.9       </td>
		<td> 95.9    </td>
		<td> A   Stack-Propagation Framework with Token-Level Intent Detection for Spoken   Language Understanding  [[pdf]](https://arxiv.org/pdf/1909.02188.pdf) </td>
		<td> https://github.com/LeePleased/StackPropagation-SLU      </td>
		<td> EMNLP  </td>
		<td></td>
</tr>
<tr>
	<td><code> SF-ID+CRF(SF first)(E et al., 2019)         </td></code>
		<td> 97.76      </td>
		<td> 95.75   </td>
		<td> A Novel   Bi-directional Interrelated Model for Joint Intent Detection and Slot   Filling [[pdf]](https://www.aclweb.org/anthology/P19-1544.pdf) </td>
		<td>                                                       </td>
		<td> ACL        </td>
		<td></td>
</tr>
<tr>
	<td><code> SF-ID+CRF(ID first)(E et al., 2019)         </td></code>
		<td> 97.09      </td>
		<td> 95.8    </td>
		<td> A Novel   Bi-directional Interrelated Model for Joint Intent Detection and Slot   Filling [[pdf]](https://www.aclweb.org/anthology/P19-1544.pdf) </td>
		<td> https://github.com/ZephyrChenzf/SF-ID-Network-For-NLU </td>
		<td> ACL        </td>
		<td></td>
</tr>
<tr>
	<td><code> Capsule-NLU(Zhang  et al. 2019)                              </td></code>
		<td> 95         </td>
		<td> 95.2    </td>
		<td> Joint Slot   Filling and Intent Detection via Capsule Neural Networks [[pdf]](https://arxiv.org/pdf/1812.09471.pdf) </td>
		<td> https://github.com/czhang99/Capsule-NLU                 </td>
		<td> ACL                                         </td>
		<td></td>
</tr>
<tr>
	<td><code> Utterance  Generation With Variational Auto-Encoder(Guo et al., 2019) </td></code>
		<td> -          </td>
		<td> 95.04   </td>
		<td> Utterance  Generation With Variational Auto-Encoder for Slot Filling in Spoken Language  Understanding [[pdf]](https://ieeexplore.ieee.org/document/8625384) </td>
		<td> -                                                       </td>
		<td> IEEE Signal Processing Letters              </td>
		<td></td>
</tr>
<tr>
	<td><code> JULVA(full)(Yoo  et al., 2019)                               </td></code>
		<td> 97.24      </td>
		<td> 95.51   </td>
		<td> Data Augmentation   for Spoken Language Understanding via Joint Variational Generation [[pdf]](https://arxiv.org/pdf/1809.02305.pdf) </td>
		<td> -                                                       </td>
		<td> AAAI                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> CM-Net(Liu  et al., 2019)                               </td></code>
		<td> 99.1      </td>
		<td> 96.20   </td>
		<td> CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding[[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf)</td>
		<td> https://github.com/Adaxry/CM-Net    </td>
		<td> EMNLP                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> Data  noising method(Kim et al., 2019)                       </td></code>
		<td> 98.43      </td>
		<td> 96.20    </td>
		<td> Data  augmentation by data noising for open vocabulary slots in spoken language  understanding [[pdf]](https://www.aclweb.org/anthology/N19-3014.pdf) </td>
		<td> -                                                       </td>
		<td> NAACL-HLT                                   </td>
		<td></td>
</tr>
<tr>
	<td><code> ACD(Zhu  et al., 2018)                                       </td></code>
		<td> -          </td>
		<td> 96.08   </td>
		<td> Concept   Transfer Learning for Adaptive Language Understanding [[pdf]](https://www.aclweb.org/anthology/W18-5047.pdf) </td>
		<td> -                                                       </td>
		<td> SIGDIAL                                     </td>
		<td></td>
</tr>
<tr>
	<td><code> A Self-Attentive Model with Gate Mechanism(Li et al., 2018)  </td></code>
		<td> 98.77      </td>
		<td> 96.52   </td>
		<td> A   Self-Attentive Model with Gate Mechanism for Spoken Language   Understanding [[pdf]](https://www.aclweb.org/anthology/D18-1417.pdf) </td>
		<td> -                                                       </td>
		<td> EMNLP                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> Slot-Gated(Goo  et al., 2018)                                </td></code>
		<td> 94.1       </td>
		<td> 95.2    </td>
		<td> Slot-Gated   Modeling for Joint Slot Filling and Intent Prediction [[pdf]](https://www.aclweb.org/anthology/N18-2118.pdf) </td>
		<td> https://github.com/MiuLab/SlotGated-SLU                 </td>
		<td> NAACL                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> DRL based Augmented Tagging System(Wang et al., 2018)        </td></code>
		<td> -          </td>
		<td> 97.86   </td>
		<td> A  New Concept of Deep Reinforcement Learning based Augmented General Sequence  Tagging System [[pdf]](https://www.aclweb.org/anthology/C18-1143.pdf) </td>
		<td> -                                                       </td>
		<td> COLING      </td>
		<td></td>
</tr>
<tr>
	<td><code> Bi-model(Wang  et al., 2018)                                 </td></code>
		<td> 98.76      </td>
		<td> 96.65   </td>
		<td> A Bi-model based   RNN Semantic Frame Parsing Model for Intent Detection and Slot Filling [[pdf]](https://arxiv.org/pdf/1812.10235.pdf) </td>
		<td> -                                                       </td>
		<td> NAACL                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> Bi-model+decoder(Wang  et al., 2018)        </td></code>
		<td> 98.99      </td>
		<td> 96.89   </td>
		<td> A Bi-model based   RNN Semantic Frame Parsing Model for Intent Detection and Slot Filling [[pdf]](https://arxiv.org/pdf/1812.10235.pdf) </td>
		<td> -                                                     </td>
		<td> NAACL      </td>
		<td></td>
</tr>
<tr>
	<td><code> Seq2Seq DA for LU(Hou et al., 2018)                          </td></code>
		<td> -          </td>
		<td> 94.82   </td>
		<td> Sequence-to-Sequence  Data Augmentation for Dialogue Language Understanding [[pdf]](https://arxiv.org/pdf/1807.01554.pdf) </td>
		<td> https://github.com/AtmaHou/Seq2SeqDataAugmentationForLU </td>
		<td> COLING                                      </td>
		<td></td>
</tr>
<tr>
	<td><code> BLSTM-LSTM(Zhu  et al., 2017)                                </td></code>
		<td> -          </td>
		<td> 95.79   </td>
		<td> ENCODER-DECODER  WITH FOCUS-MECHANISM FOR SEQUENCE LABELLING BASED SPOKEN LANGUAGE  UNDERSTANDING  [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7953243) </td>
		<td> -                                                       </td>
		<td> ICASSP                                      </td>
		<td></td>
</tr>
<tr>
	<td><code> neural  sequence chunking model(Zhai et al., 2017)           </td></code>
		<td> -          </td>
		<td> 95.86   </td>
		<td> Neural  Models for Sequence Chunking [[pdf]](https://arxiv.org/pdf/1701.04027.pdf) </td>
		<td> -                                                       </td>
		<td> AAAI                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  Model of ID and SF(Zhang et al., 2016)                </td></code>
		<td> 98.32      </td>
		<td> 96.89   </td>
		<td> A   Joint Model of Intent Determination and Slot Filling for Spoken Language   Understanding [[pdf]](https://www.ijcai.org/Proceedings/16/Papers/425.pdf) </td>
		<td> -                                                       </td>
		<td> IJCAI                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> Attention Encoder-Decoder NN (with aligned inputs)           </td></code>
		<td> 98.43      </td>
		<td> 95.87   </td>
		<td> Attention-Based   Recurrent Neural Network Models for Joint Intent Detectionand Slot   Filling      [[pdf]](https://arxiv.org/pdf/1609.01454.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> Attention  BiRNN(Liu et al., 2016)                           </td></code>
		<td> 98.21      </td>
		<td> 95.98   </td>
		<td> Attention-Based   Recurrent Neural Network Models for Joint Intent Detectionand Slot   Filling      [[pdf]](https://arxiv.org/pdf/1609.01454.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  SLU-LM model(Liu ei al., 2016)                        </td></code>
		<td> 98.43      </td>
		<td> 94.64   </td>
		<td> Joint Online   Spoken Language Understanding and Language Modeling with Recurrent Neural   Networks [[pdf]](https://arxiv.org/pdf/1609.01462.pdf) </td>
		<td> http://speech.sv.cmu.edu/software.html                  </td>
		<td> SIGDIAL                                     </td>
		<td></td>
</tr>
<tr>
	<td><code> RNN-LSTM(Hakkani-Tur  et al., 2016)                          </td></code>
		<td> 94.3       </td>
		<td> 92.6    </td>
		<td> Multi-Domain Joint Semantic Frame Parsing using   Bi-directional RNN-LSTM [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/06/IS16_MultiJoint.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> R-biRNN(Vu  et al., 2016)                                    </td></code>
		<td> -          </td>
		<td> 95.47   </td>
		<td> Bi-directional   recurrent neural network with ranking loss for spoken language   understanding      [[pdf]](https://ieeexplore.ieee.org/abstract/document/7472841/) </td>
		<td> -                                                       </td>
		<td> IEEE                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> Encoder-labeler  LSTM(Kurata et al., 2016)                   </td></code>
		<td> -          </td>
		<td> 95.4    </td>
		<td> Leveraging Sentence-level Information with  Encoder LSTM for Semantic Slot Filling [[pdf]](https://www.aclweb.org/anthology/D16-1223.pdf) </td>
		<td> -                                                       </td>
		<td> EMNLP                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> Encoder-labeler  Deep LSTM(Kurata et al., 2016)              </td></code>
		<td> -          </td>
		<td> 95.66   </td>
		<td> Leveraging Sentence-level Information with  Encoder LSTM for Semantic Slot Filling [[pdf]](https://www.aclweb.org/anthology/D16-1223.pdf) </td>
		<td>                                                         </td>
		<td> EMNLP                                       </td>
		<td></td>
</tr>
<tr>
	<td><code> 5xR-biRNN(Vu  et al., 2016)                 </td></code>
		<td> -          </td>
		<td> 95.56   </td>
		<td> Bi-directional  recurrent neural network with ranking loss for spoken language  understanding [[pdf]](https://ieeexplore.ieee.org/abstract/document/7472841/) </td>
		<td> -                                                     </td>
		<td> IEEE       </td>
		<td></td>
</tr>
<tr>
	<td><code> Data  Generation for SF(Kurata et al., 2016)                 </td></code>
		<td> -          </td>
		<td> 95.32   </td>
		<td> Labeled  Data Generation with Encoder-decoder LSTM for Semantic Slot Filling [[pdf]](https://www.isca-speech.org/archive/Interspeech_2016/pdfs/0727.PDF) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> RNN-EM(Peng  et al., 2015)                                   </td></code>
		<td> -          </td>
		<td> 95.25   </td>
		<td> Recurrent Neural   Networks with External Memory for Language Understanding [[pdf]](https://arxiv.org/pdf/1506.00195.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> RNN  trained with sampled label(Liu et al., 2015)            </td></code>
		<td> -          </td>
		<td> 94.89   </td>
		<td> Recurrent Neural Network Structured Output Prediction for   Spoken Language Understanding      [[pdf]](http://speech.sv.cmu.edu/publications/liu-nipsslu-2015.pdf) </td>
		<td> -                                                       </td>
		<td> -                                           </td>
		<td></td>
</tr>
<tr>
	<td><code> RNN(Ravuri  et al., 2015)                                    </td></code>
		<td> 97.55      </td>
		<td> -       </td>
		<td> Recurrent neural network and LSTM models for  lexical utterance classification [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/RNNLM_addressee.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> LSTM(Ravuri  et al., 2015)                                   </td></code>
		<td> 98.06      </td>
		<td> -       </td>
		<td> Recurrent neural network and LSTM models for  lexical utterance classification [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/RNNLM_addressee.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> Hybrid  RNN(Mesnil et al., 2015)                             </td></code>
		<td> -          </td>
		<td> 95.06   </td>
		<td> Using  Recurrent Neural Networks for Slot Filling in Spoken Language  Understanding [[pdf]](https://ieeexplore.ieee.org/document/6998838) </td>
		<td> -                                                       </td>
		<td> IEEE/ACM-TASLP                              </td>
		<td></td>
</tr>
<tr>
	<td><code> RecNN(Guo  et al., 2014)                                     </td></code>
		<td> 95.4       </td>
		<td> 93.22   </td>
		<td> Joint semantic utterance classification and slot filling with   recursive neural networks [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2014/12/RecNNSLU.pdf) </td>
		<td> -                                                       </td>
		<td> IEEE-SLT                                    </td>
		<td></td>
</tr>
<tr>
	<td><code> LSTM(Yao  et al., 2014)                                      </td></code>
		<td> -          </td>
		<td> 94.85   </td>
		<td> Spoken Language Understading Using Long  Short-Term Memory Neural Networks [[pdf]](https://groups.csail.mit.edu/sls/publications/2014/Zhang_SLT_2014.pdf) </td>
		<td> -                                                       </td>
		<td> IEEE                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> Deep  LSTM(Yao et al., 2014)                                 </td></code>
		<td> -          </td>
		<td> 95.08   </td>
		<td> Spoken Language Understading Using Long  Short-Term Memory Neural Networks [[pdf]](https://groups.csail.mit.edu/sls/publications/2014/Zhang_SLT_2014.pdf) </td>
		<td> -                                                       </td>
		<td> IEEE                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> R-CRF(Yao  et al., 2014)                                     </td></code>
		<td> -          </td>
		<td> 96.65   </td>
		<td> Recurrent  conditional random field for language understanding [[pdf]](https://ieeexplore.ieee.org/document/6854368) </td>
		<td> -                                                       </td>
		<td> IEEE                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> RecNN+Viterbi(Guo  et al., 2014)            </td></code>
		<td> 95.4       </td>
		<td> 93.96   </td>
		<td> Joint semantic utterance classification and slot filling with   recursive neural networks [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2014/12/RecNNSLU.pdf) </td>
		<td> -                                                     </td>
		<td> IEEE-SLT   </td>
		<td></td>
</tr>
<tr>
	<td><code> CNN  CRF(Xu et al., 2013)                                    </td></code>
		<td> 94.09      </td>
		<td> 5.42   </td>
		<td> Convolutional neural network based triangular crf for joint   intent detection and slot filling [[pdf]]((http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.642.7548&rep=rep1&type=pdf)) </td>
		<td> -                                                       </td>
		<td> IEEE                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> RNN(Yao  et al., 2013)                                       </td></code>
		<td> -          </td>
		<td> 94.11   </td>
		<td> Recurrent  Neural Networks for Language Understanding [[pdf]](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/kaisheny-338_file_paper.pdf) </td>
		<td> -                                                       </td>
		<td> InterSpeech                                 </td>
		<td></td>
</tr>
<tr>
	<td><code> Bi-dir.  Jordan-RNN(2013)                                    </td></code>
		<td> -          </td>
		<td> 93.98   </td>
		<td> Investigation  of Recurrent-Neural-Network Architectures and Learning Methods for Spoken  Language Understanding [[pdf]](https://www.isca-speech.org/archive/archive_papers/interspeech_2013/i13_3771.pdf) </td>
		<td> -                                                       </td>
		<td> ISCA                                        </td>
		<td></td>
</tr>
</tbody>
</table>
</div>


#### + Pretrained model
<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th> Model</th>
    <th>Intent Acc</th>
    <th>Slot F1</th>
    <th>Paper / Source</th>
    <th>Code link</th>
    <th>Conference</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> Co-Interactive(Qin et al., 2021)                         </td></code>
		<td> 98.0       </td>
		<td> 96.1    </td>
		<td> A Co-Interactive Transformer for Joint Slot Filling and Intent Detection  [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) </td>
		<td> https://github.com/kangbrilliant/DCA-Net      </td>
		<td> ICASSP  </td>
		<td></td>
</tr>
<tr>
	<td><code> Stack  Propagation+BERT(Qin et al., 2019)   </td></code>
		<td> 97.5       </td>
		<td> 96.1    </td>
		<td> A   Stack-Propagation Framework with Token-Level Intent Detection for Spoken   Language Understanding [[pdf]](https://arxiv.org/pdf/1909.02188.pdf) </td>
		<td> https://github.com/LeePleased/StackPropagation-SLU    </td>
		<td> EMNLP      </td>
		<td></td>
</tr>
<tr>
	<td><code> Bert-Joint(Castellucci  et al., 2019)       </td></code>
		<td> 97.8       </td>
		<td> 95.7    </td>
		<td> Multi-lingual  Intent Detection and Slot Filling in a Joint BERT-based Model [[pdf]](https://arxiv.org/pdf/1907.02884.pdf) </td>
		<td> -                                                     </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> BERT-SLU(Zhang  et al., 2019)               </td></code>
		<td> 99.76      </td>
		<td> 98.75   </td>
		<td> A Joint   Learning Framework With BERT for Spoken Language Understanding [[pdf]](https://ieeexplore.ieee.org/document/8907842) </td>
		<td> -                                                     </td>
		<td> IEEE       </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  BERT(Chen et al., 2019)              </td></code>
		<td> 97.5       </td>
		<td> 96.1    </td>
		<td> BERT for Joint   Intent Classification and Slot Filling [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) </td>
		<td> https://github.com/monologg/JointBERT                 </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  BERT+CRF(Chen et al., 2019)          </td></code>
		<td> 97.9       </td>
		<td> 96      </td>
		<td> BERT for Joint   Intent Classification and Slot Filling [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) </td>
		<td> https://github.com/monologg/JointBERT                 </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> ELMo-Light  (ELMoL) (Siddhant et al., 2019) </td></code>
		<td> 97.3       </td>
		<td> 95.42   </td>
		<td> Unsupervised   Transfer Learning for Spoken Language Understanding in Intelligent Agents [[pdf]](https://arxiv.org/pdf/1811.05370.pdf) </td>
		<td> -                                                     </td>
		<td> AAAI       </td>
		<td></td>
</tr>
</tbody >
</table>
</div>


### SNIPS

#### Non-pretrained model
<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th> Model</th>
    <th>Intent Acc</th>
    <th>Slot F1</th>
    <th>Paper / Source</th>
    <th>Code link</th>
    <th>Conference</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> Co-Interactive(Qin et al., 2021)                         </td></code>
		<td> 98.8       </td>
		<td> 95.9    </td>
		<td> A Co-Interactive Transformer for Joint Slot Filling and Intent Detection  [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) </td>
		<td> https://github.com/kangbrilliant/DCA-Net      </td>
		<td> ICASSP  </td>
		<td></td>
</tr>
<tr>
	<td><code> Graph LSTM(Zhang et al., 2021)                         </td></code>
		<td> 98.29      </td>
		<td> 95.30    </td>
		<td> Graph LSTM with Context-Gated Mechanism for Spoken Language Understanding  [[pdf]](https://ojs.aaai.org/index.php/AAAI/article/view/6499/6355) </td>
		<td> -      </td>
		<td> AAAI  </td>
		<td></td>
</tr>
<tr>
	<td><code> SF-ID  Network(E et al, 2019)                                </td></code>
		<td> 97.43      </td>
		<td> 91.43   </td>
		<td> A  Novel Bi-directional Interrelated Model for Joint Intent Detection and Slot  Filling [[pdf]](https://www.aclweb.org/anthology/P19-1544.pdf) </td>
		<td> https://github.com/ZephyrChenzf/SF-ID-Network-For-NLU        </td>
		<td> ACL                            </td>
		<td></td>
</tr>
<tr>
	<td><code> CAPSULE-NLU(Zhang  et al, 2019)                              </td></code>
		<td> 97.3       </td>
		<td> 91.8    </td>
		<td> Joint  Slot Filling and Intent Detection via Capsule Neural Networks [[pdf]](https://arxiv.org/pdf/1812.09471.pdf) </td>
		<td> https://github.com/czhang99/Capsule-NLU                      </td>
		<td> ACL                            </td>
		<td></td>
</tr>
<tr>
	<td><code> StackPropagation(Qin  et al, 2019)                           </td></code>
		<td> 98         </td>
		<td> 94.2    </td>
		<td> A  Stack-Propagation Framework with Token-Level Intent Detection for Spoken  Language Understanding     [[pdf]](https://arxiv.org/pdf/1909.02188.pdf) </td>
		<td> [https://github.com/LeePleased/StackPropagation-SLU. ](https://github.com/LeePleased/StackPropagation-SLU.) </td>
		<td> EMNLP                          </td>
		<td></td>
</tr>
<tr>
	<td><code> CM-Net(Liu  et al., 2019)                               </td></code>
		<td> 99.29      </td>
		<td> 97.15   </td>
		<td> CM-Net: A Novel Collaborative Memory Network for Spoken Language Understanding[[pdf]](https://www.aclweb.org/anthology/D19-1097.pdf)</td>
		<td> https://github.com/Adaxry/CM-Net    </td>
		<td> EMNLP                                        </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  Multiple(Gangadharaiah et al, 2019)                   </td></code>
		<td> 97.23      </td>
		<td> 88.03   </td>
		<td> Joint  Multiple Intent Detection and Slot Labeling for Goal-Oriented Dialog [[pdf]](https://www.aclweb.org/anthology/N19-1055.pdf) </td>
		<td> -                                                            </td>
		<td> NAACL                          </td>
		<td></td>
</tr>
<tr>
	<td><code> Utterance  Generation With Variational Auto-Encoder(Guo et al., 2019) </td></code>
		<td> -          </td>
		<td> 93.18   </td>
		<td> Utterance  Generation With Variational Auto-Encoder for Slot Filling in Spoken Language  Understanding        [[pdf]](https://ieeexplore.ieee.org/document/8625384) </td>
		<td> -                                                            </td>
		<td> IEEE Signal Processing Letters </td>
		<td></td>
</tr>
<tr>
	<td><code> Slot  Gated Intent Atten.(Goo et al, 2018)                   </td></code>
		<td> 96.8       </td>
		<td> 88.3    </td>
		<td> Slot-Gated   Modeling for Joint Slot Filling and Intent Prediction [[pdf]](https://www.aclweb.org/anthology/N18-2118.pdf) </td>
		<td> https://github.com/MiuLab/SlotGated-SLU                      </td>
		<td> NAACL                          </td>
		<td></td>
</tr>
<tr>
	<td><code> Slot  Gated Fulled Atten.(Goo et al, 2018)                   </td></code>
		<td> 97         </td>
		<td> 88.8    </td>
		<td> Slot-Gated  Modeling for Joint Slot Filling and Intent Prediction [[pdf]](https://www.aclweb.org/anthology/N18-2118.pdf) </td>
		<td> https://github.com/MiuLab/SlotGated-SLU                      </td>
		<td> NAACL                          </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  Variational Generation + Slot Gated Intent Atten(Yoo et al., 2018) </td></code>
		<td> 96.7       </td>
		<td> 88.3    </td>
		<td> Data  Augmentation for Spoken Language Understanding via Joint Variational  Generation [[pdf]](https://arxiv.org/pdf/1809.02305.pdf) </td>
		<td> -                                                            </td>
		<td> AAAI                           </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  Variational Generation + Slot Gated Full Atten(Yoo et al., 2018) </td></code>
		<td> 97.3       </td>
		<td> 89.3    </td>
		<td> Data Augmentation  for Spoken Language Understanding via Joint Variational Generation [[pdf]](https://arxiv.org/pdf/1809.02305.pdf) </td>
		<td> -                                                            </td>
		<td> AAAI                           </td>
		<td></td>
</tr>
</tbody >
</table>
</div>



#### + Pretrained model
<div style="overflow-x: auto; overflow-y: auto; height: auto; width:100%;">
<table style="width:100%" border="2">
<thead>
  <tr>
    <th> Model</th>
    <th>Intent Acc</th>
    <th>Slot F1</th>
    <th>Paper / Source</th>
    <th>Code link</th>
    <th>Conference</th>
  </tr>
</thead>
<tbody >
<tr>
	<td><code> Co-Interactive(Qin et al., 2021)                         </td></code>
		<td> 98.8       </td>
		<td> 97.1    </td>
		<td> A Co-Interactive Transformer for Joint Slot Filling and Intent Detection  [[pdf]](https://arxiv.org/pdf/2010.03880.pdf) </td>
		<td> https://github.com/kangbrilliant/DCA-Net      </td>
		<td> ICASSP  </td>
		<td></td>
</tr>
<tr>
	<td><code> StackPropagation  + Bert(Qin et al, 2019)       </td></code>
		<td> 99         </td>
		<td> 97      </td>
		<td> A   Stack-Propagation Framework with Token-Level Intent Detection for Spoken   Language Understanding [[pdf]](https://arxiv.org/pdf/1909.02188.pdf) </td>
		<td> [https://github.com/LeePleased/StackPropagation-SLU. ](https://github.com/LeePleased/StackPropagation-SLU.) </td>
		<td> EMNLP      </td>
		<td></td>
</tr>
<tr>
	<td><code> Bert-Joint(Castellucci  et al, 2019)            </td></code>
		<td> 99         </td>
		<td> 96.2    </td>
		<td> Multi-lingual  Intent Detection and Slot Filling in a Joint BERT-based Mode [[pdf]](https://arxiv.org/pdf/1907.02884.pdf) </td>
		<td> -                                                            </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> Bert-SLU(Zhang  et al, 2019)                    </td></code>
		<td> 98.96      </td>
		<td> 98.78   </td>
		<td> A Joint Learning  Framework With BERT for Spoken Language Understanding [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8907842) </td>
		<td> -                                                            </td>
		<td> IEEE       </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  BERT(Chen et al, 2019)                   </td></code>
		<td> 98.6       </td>
		<td> 97      </td>
		<td> BERT for Joint   Intent Classification and Slot Filling [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) </td>
		<td> https://github.com/monologg/JointBERT                        </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> Joint  BERT + CRF(Chen et al, 2019)             </td></code>
		<td> 98.4       </td>
		<td> 96.7    </td>
		<td> BERT  for Joint Intent Classification and Slot Filling [[pdf]](https://arxiv.org/pdf/1902.10909.pdf) </td>
		<td> https://github.com/monologg/JointBERT                        </td>
		<td> arXiv      </td>
		<td></td>
</tr>
<tr>
	<td><code> ELMo-Light(Siddhant  et al, 2019)               </td></code>
		<td> 98.38      </td>
		<td> 93.29   </td>
		<td> Unsupervised   Transfer Learning for Spoken Language Understanding in Intelligent Agents         [[pdf]](https://arxiv.org/pdf/1811.05370.pdf) </td>
		<td> -                                                            </td>
		<td> AAAI       </td>
		<td></td>
</tr>
<tr>
	<td><code> ELMo(Peters  et al, 2018;Siddhant et al, 2019 ) </td></code>
		<td> 99.29      </td>
		<td> 93.9    </td>
		<td> Deep   contextualized word representations      [[pdf]](https://arxiv.org/pdf/1802.05365.pdf)Unsupervised Transfer Learning for Spoken Language Understanding in   Intelligent Agents [[pdf]](https://arxiv.org/pdf/1811.05370.pdf) </td>
		<td> -                                                            </td>
		<td> NAACL/AAAI </td>
		<td></td>
</tr>
</tbody>
</table>
</div>
-->

