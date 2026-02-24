# Collect Feedback

See the implementation in [collect-feedback.json](collect-feedback.json).

This simple adaptive card will post a [MessageEvent](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-send-event-activities) that can be used trigger a topic, extract the data, and log to SharePoint, Teams, Azure Application Insights, etc..

## MessageEvent Schema

A simple schema with enough data from from the adaptive card to distinguish the feedback.

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
