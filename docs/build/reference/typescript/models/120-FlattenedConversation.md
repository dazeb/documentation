---
title: FlattenedConversation | TypeScript SDK
---


# FlattenedConversation

This is a flattend version of the Convsersation for DAG-Safety.  This will hold together a conversation. Ie allthe message within a conversation.  All the additional properties on here used on here like(anchors/assets) are used for context that will seed the conversation.  model is a calculated property, and will be the model of the last message sent if applicable.  summaries: on the top level here will simply be used to associate a conversation and a summary(this is not used for grounding), grounding.summaries will be used for this.(TODO)

## Properties

Name | Type
------------ | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema)
**id** | **string**
**name** | **string**
**created** | [**GroupedTimestamp**](GroupedTimestamp)
**updated** | [**GroupedTimestamp**](GroupedTimestamp)
**deleted** | [**GroupedTimestamp**](GroupedTimestamp)
**favorited** | **boolean**
**application** | [**Application**](Application)
**annotations** | [**FlattenedAnnotations**](FlattenedAnnotations)
**messages** | [**FlattenedConversationMessages**](FlattenedConversationMessages)
**model** | [**ReferencedModel**](ReferencedModel)
**assets** | [**FlattenedAssets**](FlattenedAssets)
**websites** | [**FlattenedWebsites**](FlattenedWebsites)
**anchors** | [**FlattenedAnchors**](FlattenedAnchors)
**type** | [**ConversationTypeEnum**](ConversationTypeEnum)
**grounding** | [**ConversationGrounding**](ConversationGrounding)
**score** | [**Score**](Score)
**pipeline** | [**QGPTPromptPipeline**](QGPTPromptPipeline)
**demo** | **boolean**
**summaries** | [**FlattenedWorkstreamSummaries**](FlattenedWorkstreamSummaries)


