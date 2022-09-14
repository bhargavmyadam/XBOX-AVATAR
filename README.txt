Copyright (C) Microsoft Research 
This copy of CLex Lexicon is to be used for research purposes only. Do not redistribute the data. 

Contacts: Mark Yatskar, University of Washington, Computer Science & Engineering (my89@cs.washington.edu)
	  Svitlana Volkova, Johns Hopkins University, Center for Language and Speech Processing (svitlana@jhu.edu)
  
Section I citation:
	Learning to Relate Literal and Sentimental Descriptions of Visual Properties. Mark Yatskar, Svitlana Volkova, Asli Celikyilmaz, Bill Dolan, Luke Zettlemoyer,
	In Proceedings of NAACL-HLT, Atlanta, USA, 2013.

Section II citation: 
	CLex: A Lexicon for Exploring Color, Concept and Emotion Associations in Language. Svitlana Volkova, William B. Dolan, and Theresa Wilson,
	In Proceeding EACL, Stroudsburg, PA, USA, 2012, 306-314. 

--------------------------------------------------------------------
Section I. Literal and Sentimental Avatar/Object Descriptions
--------------------------------------------------------------------


This dataset contains publicly generated responses and may contain terms that some may consider offensive, indecent or otherwise objectionable. Microsoft has not reviewed or modified the content of the dataset. Microsoft is providing this dataset as a convenience and is not responsible or liable for any inappropriate content in the dataset. Use of the dataset is at your own risk and discretion.

AssetNameToXBoxImageLabelMapping
--------------------------------
	666 rows and 2 tab separated columns
	#1 AssetName
	#2 XBoxLabel

AbsoluteDescriptionsEmotions
----------------------------
	50 descriptions/emotions per asset
	33,216 rows and 3 tab separated columns
	#1 AssetName
	#2 Emotions
	#3 Descriptions	

RelativeDescriptionsEmotions
---------------------------- 
	50 descriptions per asset pair for particular facial features: eyebrow, ear, lips, nose, chin
	47,713 rows and 7 tab separated columns
	#1 CategoryName
	#2 AssetName1
	#3 AssetName2
	#4 Description that we get when we change FROM AssetName1 TO AssetName2
	#5 Emotion that we get when we change FROM AssetName1 TO AssetName2
	#6 Description that we get when we change FROM AssetName2 TO AssetName1
	#7 column is an emotion that we get when we change FROM AssetName2 TO AssetName1

MultilingualDescriptionsEmotions
--------------------------------
	13+ languages with more than 100 annotations
	13,252 rows and 5 tab separated columns
	#1 AssetName
	#2 Descriptions	
	#3 Emotions
	#4 Language
	#5 Country

FullAvatarDescriptions
----------------------
	20 one paragraph descriptions/emotions per avatar
	2000 rows and 3 tab separated columns
	#1 AvatarId
	#2 One paragraph descriptions
	#3 Emotions

FullAvatarToAssetNameMapping
----------------------------
	1115 rows and 3 tab separated columns	
	#1 AvatarId
	#2 CategoryName
	#3 AssetName
GamerAvatarToAssetNameMapping
-----------------------------
	22661 rows and 3 tab separated columns
	#1 GamerAvatarId
	#2 Category name
	#3 AssetName

GamerAvatarSentimental
----------------------
	9248 rows and 26 tab separated columns
	#1 GamerAvatarId
	#2-#7    Answers to the question "What is the emotional state of this avatar?"
	#8-#13   Answers to the question "What might this avatar care about?"
	#14-#19  Answers to the question "What might this avatar do for a living?"
	#20-#26  Answers to the question "What are some general phrases that describe their overall appearance?"

--------------------------------------------------------------------
Section II. Color, Emotion, Concept Association Lexicon (CLex v.1.0)
--------------------------------------------------------------------
Color-emotion-concept association lexicon CLex was created via crowdsourcing during the summer of 2011. CLex contains over 2,3K color terms, over 3K affect terms including mood, cognitive state, behavior and attitude, and almost 2K concepts. Workers on Mechanical Turk were showed a swatch for one RGB value and paid to name the color, describe emotions this color evokes and define a set of concepts associated with that color. The result is a set of names of 132 RGB values, emotions and concepts associated with them. We expect this data to be useful for investigating variance in annotations for color-emotion-concept associations among workers from different cultural and linguistic backgrounds. Color-concept-emotion associations in CLex have the potential to enhance human-computer interactions in many real- and virtual-world domains, e.g., online shopping, and avatar construction in gaming environments. 


CLex v.1.0
----------
	15,203 rows and 7 tab separated columns
	#1 Experiment - can be either 0 or 1; 0 corresponds to the experiment where only a color swatch was shown and 1 corresponds to the experiment where BOTH color swatch and a facial feature colored with the color were shown
	#2 RGB - RGB value
	#3 Category - there 7 categories in the data that correspond to 7 facial features (Eye_Shadow, Eye, FacialFeature, Hair, Lips, Skin, and FacialMask)
	#4 Answer country - country of the annotator (if N/A then country was not provided)
	#5 Answer color - color named associated with RGB value
	#6 Answer emotions - one or more affect terms separated by space or comas associated with RGB value
	#7 Answer objects - one or more concepts/objects separated by space or comas associated the RGB value
