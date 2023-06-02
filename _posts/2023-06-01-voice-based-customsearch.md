---
layout: post
title: Voice Based Custom Search
date: 2023-06-01
description: Voice Based Custom Search
tags: ai ml
giscus_comments: false
related_posts: false
toc:
  beginning: true
---

# Abstract
A Hybrid Ionic mobile app ([voice-based-customsearch](https://github.com/vinapp/voice-based-customsearch)) that accepts Indic voice-based commands to search the Indic (domain) scoped data. The Indic domain data includes data such as music/tourism/theertha-stala/spiritual/yoga/etc. Here the voice to text conversion happens via JS WebSpeech API's. Also, the search engine includes custom Google search engine, Wikipedia search engine or similar one (one or more of these). The Google custom Search helps in creating our own search engine for a choosen topic collected from a group of websites of our choosing.

# Motivation
- Explore the client and service-side aspects of voice-to-text & tts.
- Investigate existing publicly available search engines or APIs for querying domain-specific public data, rather than building our own.
- Extend the search to include morphological analysis and generation for Indian languages to improve the search engine results. The output of the search engine depends on the input words. If a word is provided in an inflected form and is not present in the search engine's lexicon, it will affect the search engine's output.
- One of the most common use case that people want is to be able to search for information by speaking a query into a device.
- More/Extend (Own Pretrained ASR model + TTS + Q/A for websites)

# High Level Flow
<img width="828" alt="image" src="https://github.com/vinapp/voice-based-customsearch/assets/8567548/469a817a-00da-4691-b346-0422286b968d">

# ASR/TTS – WebSpeech API – Backend flow
- Web Speech API is a web technology specification that is developed and maintained by the World Wide Web Consortium (W3C)
- Web Speech API is a JavaScript API that allows developers to incorporate speech recognition and synthesis capabilities into web - applications.
- The implementation of the Web Speech API can vary slightly between different browsers
- Each browser implements the Web Speech API using its own underlying speech recognition and synthesis engines
- Google Chrome's speech recognition engine requires an active internet connection to work, as it relies on cloud-based speech recognition technology that processes the audio input on remote servers.
- Speech recognition engines, such as the one used in Windows 10, can work offline to some extent by using pre-installed language models and recognition algorithm

# API’s (Search & Web Speech)
- Web Search API’s
  - [https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition)
  - [https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis)

- Tensor flow JS:
  - [https://www.tensorflow.org/lite](https://www.tensorflow.org/lite)
  - [https://github.com/tensorflow/tfjs](https://github.com/tensorflow/tfjs)
  - [https://github.com/tulasiram58827/TTS_TFLite/tree/main/models](https://github.com/tulasiram58827/TTS_TFLite/tree/main/models)

- Google Custom Search
  - [https://developers.google.com/custom-search/v1/overview](https://developers.google.com/custom-search/v1/overview)

- Wiki Search
  - [https://www.mediawiki.org/wiki/API:Search](https://www.mediawiki.org/wiki/API:Search)
  - [https://kn.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=ಶ್ರೀರಂಗ&sroffset=10](https://kn.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=ಶ್ರೀರಂಗ&sroffset=10)

- Wiki Geo Search
  - [https://www.mediawiki.org/wiki/API:Search](https://www.mediawiki.org/wiki/API:Search)
  - [https://kn.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=ಶ್ರೀರಂಗ&sroffset=10](https://kn.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=ಶ್ರೀರಂಗ&sroffset=10)
  - [https://en.wikipedia.org/w/api.php?action=query&prop=coordinates&format=json&titles=Tirupati](https://en.wikipedia.org/w/api.php?action=query&prop=coordinates&format=json&titles=Tirupati)
  - [https://en.wikipedia.org/w/api.php?action=query&list=geosearch&format=json&gscoord=10.87|78.68&gsradius=10000&gslimit=5](https://en.wikipedia.org/w/api.php?action=query&list=geosearch&format=json&gscoord=10.87|78.68&gsradius=10000&gslimit=5)

- Open Search API’s
  - [https://www.mediawiki.org/wiki/API:Search](https://www.mediawiki.org/wiki/API:Search)

# Search Engine - Configuration
<img width="910" alt="image" src="https://github.com/vinapp/voice-based-customsearch/assets/8567548/693e4bfd-c40d-476d-aacb-c4b1afcc4135">

# Search Options
<img width="809" alt="image" src="https://github.com/vinapp/voice-based-customsearch/assets/8567548/224853cf-6e16-40ed-b695-5c85de4eb7a1">

# Reference links
  ### Custom Google Search
  - [https://developers.google.com/custom-search/v1/overview](https://developers.google.com/custom-search/v1/overview)
  - [https://programmablesearchengine.google.com/controlpanel/all](https://programmablesearchengine.google.com/controlpanel/all)
  ### Maps
  - [https://openlayers.org/](https://openlayers.org/)
  - [https://openlayers.org/en/latest/examples/](https://openlayers.org/en/latest/examples/)
  - [https://wiki.openstreetmap.org/wiki/Main_Page](https://wiki.openstreetmap.org/wiki/Main_Page)

# Source Code
  - [https://github.com/vinapp/voice-based-customsearch](https://github.com/vinapp/voice-based-customsearch)
