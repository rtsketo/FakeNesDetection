# Fake News Detection

## Description
<p align="justify">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fake news is a type of deliberate misinformation that spreads via the media to either influence the public’s opinion or gain financially. Although fake news used primarily to spread through traditional media, the wide adaption of internet services over the past years has shifted the main source of misinformation. Internet has allowed information to propagate faster than ever before, but it has also enabled a completely new way to publish, share and consume news with very little to none regulation or editorial standards. User generated content far surpasses the amount of traditional media content resulting in an overload of the current online news environment. In such an environment, it has become extremely difficult for the average reader to evaluate the credibility of an article and, to some extent, to distinguish between content generated by users and content generated by journalists. The need of new technologies and automated tools arises, as fact checking and source verification becomes a time-consuming process. Various approaches of identifying deception in articles have shown very promising results. Patterns, like the frequency of a word’s appearance or a phrase’s syntactic structure, can give away the author’s underlying intentions. The goal achieved in this thesis is the exploration of possible ways we can detect deception in articles and the development of an easy to use and train application, which is able to check the veracity of either plain text or a web-page that contains a news article written in Greek.</p>
<br>

## Usage
1) Make sure the files are in the proper directory (see *File Structure*).

2) Run the app using FakeDetection.bat or the command:

        java -jar fakeDetection.jar
  
3) Test the app using AccuracyTester.bat or the command:

        java -cp FakeDetection.jar Test.Tester <repetitions>
  *Example*: java -cp FakeDetection.jar Test.Tester 100

<br>

## Files
src: Application's source code.<br>
lib: Library dependencies. Uploaded for consistency.<br>

Models: Models needed for PoS-tagging.<br>
News: A collection of news articles pre-categorized.<br>

AccuracyTester.bat:	Batch file for starting the accuracy test.<br>
FakeDetection.bat: Batch file for starting the application.<br>

Trained Dbase.7z: A sample of an already trained database.<br>
FakeDetection.jar: Appication compiled into jar file.<br>


<br>


## File Structure
root<br>
|-- Models<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- POS<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|-- English.DICT<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;\`-- English.RDR<br>
|&nbsp;&nbsp;&nbsp;&nbsp;\`-- UniPOS/UD_Greek<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;|-- el-upos.DICT<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;\`-- el-upos.RDR<br>
|-- News<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- fake.txt<br>
|&nbsp;&nbsp;&nbsp;&nbsp;\`-- good.txt<br>
|-- lib<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- commons-io-2.6.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- commons-lang3-3.7.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- commons-logging-1.2.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- guava-23.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- java-json.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- jaxb-api-2.3.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- jsoup-1.11.2.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- language-el-4.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- languagetool-core-4.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- morfologik-fsa-2.1.4.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- morfologik-speller-2.1.4.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- morfologik-stemming-2.1.4.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- morphology-el-1.0.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- opennlp-tools-1.8.4.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;|-- segment-2.0.0.jar<br>
|&nbsp;&nbsp;&nbsp;&nbsp;\`-- sqlite-jdbc-3.20.0.jar<br>
|-- AccuracyTester.bat<br>
|-- FakeDetection.bat<br>
|-- FakeDetection.jar<br>
\`-- edu.db<br>

**Notice:** edu.db is extracted from *Trained Dbase.7z*
