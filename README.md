# Meddle
A general-purpose metaservice providing property storage and injection to spice up any web API.

## Basics

Meddle is a proxy service created to provide a simple set of metadata operations to other APIs.

There are two main parts to Meddle:

### Meddle Map

Meddle Map provides the ability to manipulate the responses from external resources. Like the `map` operation in functional programming, Meddle provides a set of operations to transform responses.

#### Examples

* Inject a `"fetched_at": now()` property to a JSON response
* Make secondary API requests to resources in the initial response

### Meddle Store

Meddle Store is key-value storage interface built specifically for persisting data related to the resources fetched through Meddle Map. Store makes it dead-simple to effectively create new and persisted properties for any web API.

The combination of Map + Store lets you effetively add new features to external APIs.

#### Examples

* Add a `"last_viewed"` or a "`visit_count"` property to a list of photos returned from Flickr's API.
* Implement a feature in a news app to persist which articles your user reads.
