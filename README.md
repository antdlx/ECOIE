# ECOIE
Efficient Chinese Open Information Extraction with Syntactic Constraints

Requirement:
  JRE 1.8+

Input-data:
  Input data have to be stored in a file, each line contains a sentence. The input data should firstly be 
  pre-processed by a Chinese word segmenter and POS tagger. The POS tagger have to tag words with CTB POS 
  tag set. The Stanford word segmenter and POS tagger is recommended to be used for pre-processing.
  After pre-processing, the input data have to in the following format:
  word1#POS tag1'space'word2#POS tag2'space'...wordN#POS tagN
  For example:
  我#PN 爱#VV 北京#NR 天安门#NR

Run:
  execute command: java -jar ecoie.jar config/config
  
  before you run ecoie, change the path in the config file first, MENTION, the path should not contain ":"

Config file:
  The parameters to run ecoie is provided by the config file
  #path to the config directory under the main directory of this package
  confdir:config/
  #encoding format of input data
  encoding:UTF-8
  #segmented and POS tagged input file, one sentence each line is better.
  filein:test/example-input
  #threshold for syntactic constrain, it's tuned on a randomly selected development set, better not change it
  frethreshold:9
  #print time information during execution 
  needtimedetail:1
  #path to the table of syntactic constraint
  phrasetable:config/phrase-table
  
Contact:
  hennande@gmail.com
  
This project is supervised by Professor Li Zhoujun, The Institute of Intelligent Information Processing, Beihang University
