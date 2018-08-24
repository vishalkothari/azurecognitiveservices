---
services: cognitive-services,speech, language understanding, text analytics
platforms: dotnet
---

# Microsoft Cognitive Services Sample
This repo contains the Windows client library & sample for using Speech-to-Text in the Microsoft Bing Speech API, an offering within [Microsoft Cognitive Services](https://www.microsoft.com/cognitive-services), formerly known as Project Oxford.
* [Learn about the Bing Speech API](https://www.microsoft.com/cognitive-services/en-us/speech-api)
* [Learn about the Language understanding] https://azure.microsoft.com/en-in/services/cognitive-services/language-understanding-intelligent-service/
* [Learn about the Text Analytics] https://azure.microsoft.com/en-in/services/cognitive-services/text-analytics/
* [Read the documentation](https://www.microsoft.com/cognitive-services/en-us/speech-api/documentation/overview)
* [Find more SDKs & Samples](https://www.microsoft.com/cognitive-services/en-us/SDK-Sample?api=bing%20speech)


## The Client Library
The Speech-to-Text client library is a thin C\# client wrapper for Bing Speech API. 

The easiest way to use this client library is to get microsoft.projectoxford.speechrecognition package from [nuget](<http://nuget.org>). There are two nuget packages. One is for x86 build, and one is for x64 build.
 * For x86 package, please go to [Speech Recognition API x86 Package in nuget](https://www.nuget.org/packages/Microsoft.ProjectOxford.SpeechRecognition-x86/) for more details.
 * For x64 package, please go to [Speech Recognition API x64 Package in nuget](https://www.nuget.org/packages/Microsoft.ProjectOxford.SpeechRecognition-x64/) for more details.


## The Sample
This sample is a Windows WPF application to demonstrate the use of Speech-to-Text in the Bing Speech API. It demonstrates the following features using a wav file or external microphone input:
 * Short-form recognition
 * Long-form dictation
 * Recognition with intent

### Build the sample
 1. Start Microsoft Visual Studio 2015 and select `File > Open >
    Project/Solution`.

 2. Navigate to the folder where you cloned the repository.

 3. Double-click the Visual Studio 2015 Solution (.sln) file
    SpeechToText-WPF-Sample.

 4. Choose the build flavor to be x64. This is important because the sample is using Microsoft.ProjectOxford.SpeechRecognition-x64 nuget package by default.

 5. Press Ctrl+Shift+B, or select `Build > Build Solution`.

For intent recognition to work, you need to sign up [Language Understanding Intelligent Service (LUIS)](<https://www.microsoft.com/cognitive-services/en-us/sign-up>). Please put your LUIS App ID and Subscription ID in app.config file. app.config file can be located from Solution Explorer.
For Text analytics to work, add text analytics key in MainWindow.xaml.cs

<img src="SampleScreenshots/SampleRunning1.png" width="100%"/>

### Run the sample
After the build is complete, press F5 to run the sample.

First, you must obtain a Speech API subscription key by [following the instructions on our website](<https://www.microsoft.com/cognitive-services/en-us/sign-up>).

Locate the text edit box saying "Paste your subscription key here to start" on the top right corner. Paste your subscription key. You can choose to persist your subscription key in your machine by clicking "Save Key" button. When you want to delete the subscription key from the machine, click "Delete Key" to remove it from your machine.

Microsoft will receive the audio you upload and may use them to improve the Bing Speech API and related services. By submitting an audio, you confirm you have consent from everyone in it.

