# MassTransit.Extensions

A collection of extensions and tools for the MassTransit library.

## How did you come up with this project

I've been using the MassTransit library for a few months now, and despite its advantages, it has some weaknesses that make life miserable. First of all, I would like to approach two elements that can be useful to me in my current work:
 * Support for RabbitMQ in Azure Functions - it is not possible to use providers other than Azure Service Bus/Event Hub and the developers do not want to do so. This extension will make at least local work and integration testing easier. For local work, you can get around this by using your own developer Azure ServiceBus or emulating it, I would like to simplify this with one option-driven solution.
 * ARM/Bicep generator for Azure Service BusTopics, Subscriptions, Queue - currently MassTransit needs to have high permissions to Azure Service Bus to work properly. The developers' assumptions are that MassTransit if it needs some structures on the Azure Service Bus side will be able to create them itself. I would like to create a tool with which it will be possible to generate scripts for the Azure CLI to create the necessary structures in Azure Service Bus, thus it will be possible to lower access permissions to Azure Service Bus.

As the work progresses, it is possible that there will be more extensions to MassTransit that I would like to develop.