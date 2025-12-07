# Scope Definition

It may seem that defining a scope for multimodal audio models is a relatively straightforward task. 

But in reality, it invites some nuance. 

Audio encompasses different things like speech and music. 

Consider, for example, a music generation model such as Suno or BARK.

Even if we add the qualifier: "audio multimodal means that it must accept audio as an *input* modality" we fail to exclude music-music models (say, a model that takes a song and remixes it to another genre!)

These are audio multimodal models. But beyond the differences in use case, they can be distinguished from audio multimodal models that support audio both as an input and output modality, like in the previous example. 

I'm personally interested in this niche area of multimodal for the use-cases outlined in the README. 

Therefore, the operative scope here is biased towards "audio multimodal" meaning processing *human speech* in order to produce different outputs from it - but mostly textual - which go beyond the act of simply tokenising it into text verbatim. 