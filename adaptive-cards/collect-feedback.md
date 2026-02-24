# Collect Feedback

See the implementation in [collect-feedback.json](collect-feedback.json).

This simple adaptive card will post a [MessageEvent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-send-event-activities) that can be used trigger a topic, extract the data, and log to SharePoint, Teams, Azure Application Insights, etc..

<img src="https://github.com/CopilotSWATTeam/copilot-studio-patterns/blob/main/adaptive-cards/media/collect-feedback1.png?raw=true" width="250">

## MessageEvent Schema

he structure is simple *intentionally*; no need to duplicate code if not needed. Additional information (User ID, etc.) can be collected in the handling topic.

``` json
{
    "MessageEvent": "CollectFeedback",
    "Like": true,
    "Prompt": "System.Activity.Text",
    "Answer": "Answer"
}
```

### Variations on a Theme

- Implement a "star" rating system.
- Collect textual feedback.
