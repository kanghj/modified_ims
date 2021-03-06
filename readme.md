IMS making use of Word2Vec
=========================

This is an extension of IMS developed by the NUS NLP Group.

Zhong, Zhi, and Hwee Tou Ng. "It makes sense: A wide-coverage word sense disambiguation system for free text." Proceedings of the ACL 2010 System Demonstrations. Association for Computational Linguistics, 2010.


It can now make use of word embeddings!

First setup IMS according to the IMS setting up guide in their readme.
The libs files, examples files, and the ~~models~~ files should be downloaded.
This should be downloaded too: http://commons.apache.org/proper/commons-lang/download_lang.cgi, and the entire folder placed in the libs folder. 
 
http://nlp.stanford.edu/software/stanford-parser-full-2015-12-09.zip should be downloaded too. stanford-parser-3.6.0-models.jar, stanford-parser.jar, slf4j-api.jar and slf4j-simple.jar placed in the libs folder.

The following files will be helpful for SE-2007: WordNet 2.1 should be downloaded, its dict directory placed in lib/dict21. In libs/prop.xml, under jnwl_properties/dictionary/param[name=file_manager]/param[name=dictionary_path], the value should be changed to lib/dict21. 


For running the code here, make 2 empty directories, trainedDir and resultDir.
From the Makefile here,
* To run on Senseval2 Lexical Sample task, run `make senseval2`.
* To run on Senseval2 Lexical Sample task, run `make senseval3`.

* To run on Senseval2 All Words task, run `make test_all_words_se2` (if there are any permissions error when writing to file, make a file `SE2_AW_output`)
* To run on Senseval3 All Words task, run `make test_all_words_se3`(if there are any permissions error when writing to file, make a file `SE3_AW_output`)
* For Semeval-2007, `make test_fine_all_words_SE2007` and `make test_coarse_all_words_SE2007` (if there are permissions error when writing to file, make files `SE2007_AW_output` and `SE2007_AW_Coarse_output`)

* for CLWSD, `make test_CLWSD_Context_Sum` and `make test_CLWSD_IMS`

#Notes about files:
`./corpora` contains the senseval2 files
`./EnglishLS.train`, `./EnglishLS.test` and `./EnglishAW.text` contains the senseval3 files

`semeval-2007` and `semeval-2007-coarse-grained-all-words` contains semeval-2007 files

`compiled_data_annotations` contains files for the created CLWSD task. 

model files for monolingual wsd (senseval2, 3, 2007) can be downloaded from:
`https://gitlab.com/kanghongjin/ims_oneMillionTrainedDirContextSumWN21.git`
`https://gitlab.com/kanghongjin/ims_oneMillionTrainedDirWN21.git`
`https://gitlab.com/kanghongjin/oneMillionTrainedDirContextSum.git `

model files for CLWSD can be downloaded from:
`https://gitlab.com/kanghongjin/UMCorpus_ContextSum`
`https://gitlab.com/kanghongjin/UMCorpus_IMS`


