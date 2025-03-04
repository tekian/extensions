
# ContextualOptions

| Diagnostic ID     | Description |
| :---------------- | :---------- |
| `CTXOPTGEN000` | Options context classes can't be static |
| `CTXOPTGEN001` | Options context types must be partial |
| `CTXOPTGEN002` | The options context type does not have usable properties |
| `CTXOPTGEN003` | The options context cannot be a ref-like type |


# Design

| Diagnostic ID     | Description |
| :---------------- | :---------- |
| `AUTOCLIENTGEN001` | API client interfaces must not be nested types |
| `AUTOCLIENTGEN002` | REST API client does not have methods defined |
| `AUTOCLIENTGEN003` | An API method must not contain more than one REST method attribute |
| `AUTOCLIENTGEN004` | Invalid API method return type |
| `AUTOCLIENTGEN005` | API methods can't be generic |
| `AUTOCLIENTGEN006` | The current HTTP method does not support the body tag |
| `AUTOCLIENTGEN007` | API methods must not be static |
| `AUTOCLIENTGEN008` | HTTP method missing |
| `AUTOCLIENTGEN009` | The API interface cannot be generic |
| `AUTOCLIENTGEN010` | Invalid API interface name |
| `AUTOCLIENTGEN011` | Duplicate body attribute |
| `AUTOCLIENTGEN012` | URL parameter missing from path |
| `AUTOCLIENTGEN013` | REST API method has more than one cancellation token |
| `AUTOCLIENTGEN014` | Missing CancellationToken from REST API method |
| `AUTOCLIENTGEN015` | API method path should not contain query |
| `AUTOCLIENTGEN016` | A REST API method's request name must be unique |
| `AUTOCLIENTGEN017` | Invalid HttpClient name |
| `AUTOCLIENTGEN018` | Invalid dependency name |
| `AUTOCLIENTGEN019` | Invalid header name |
| `AUTOCLIENTGEN020` | Invalid header value |
| `AUTOCLIENTGEN021` | Invalid REST method path |
| `AUTOCLIENTGEN022` | Invalid request name |


# ExtraAnalyzers

| Diagnostic ID     | Category | Description |
| :---------------- | :---------- | :---------- |
| `EA0000` | Performance  | Use source generated logging methods for improved performance |
| `EA0001` | Performance  | Perform message formatting in the body of the logging method |
| `EA0002` | Reliability  | Use 'System.TimeProvider' to make the code easier to test |
| `EA0003` | Performance  | Use the character-based overloads of 'String.StartsWith' or 'String.EndsWith' |
| `EA0004` | Performance  | Make types declared in an executable internal |
| `EA0005` | Performance  | Consider using an array instead of a collection |
| `EA0006` | Performance  | Replace uses of 'Enum.GetName' and 'Enum.ToString' for improved performance |
| `EA0007` | Performance  | Use 'System.ValueTuple' instead of 'System.Tuple' for improved performance |
| `EA0008` | Performance  | Use generic collections instead of legacy collections for improved performance |
| `EA0009` | Performance  | Use 'System.MemoryExtensions.Split' for improved performance |
| `EA0010` | Correctness  | Fire-and-forget async call inside a 'using' block |
| `EA0011` | Performance  | Consider removing unnecessary conditional access operator (?) |
| `EA0012` | Performance  | Consider removing unnecessary null coalescing assignment (??=) |
| `EA0013` | Performance  | Consider removing unnecessary null coalescing operator (??) |
| `EA0014` | Resilience  | The async method doesn't support cancellation |


# Experiments

As new functionality is introduced to this repo, new in-development APIs are marked as being experimental. Experimental APIs offer no
compatibility guarantees and can change without notice. They are usually published in order to gather feedback before finalizing
a design.

You may use experimental APIs in your application, but we advise against using these APIs in production scenarios as they may not be
fully tested nor fully reliable. Additionally, we strongly recommend that library authors do not publish versions of their libraries
that depend on experimental APIs as this will quite possibly lead to future breaking changes and diamond problems.

If you use experimental APIs, you will get one of the diagnostic shown below. The diagnostic is there to let you know you're
using such an API so that you can avoid accidentally depending on experimental features. You may suppress these diagnostics
if desired.


| Diagnostic ID     | Description |
| :---------------- | :---------- |
| `EXTEXP0001` | Resilience experiments |
| `EXTEXP0002` | Compliance experiments  |
| `EXTEXP0003` | Telemetry experiments |
| `EXTEXP0004` | TimeProvider experiments |
| `EXTEXP0005` | AutoClient experiments |
| `EXTEXP0006` | AsyncState experiments |
| `EXTEXP0007` | Health check experiments |
| `EXTEXP0008` | Resource monitoring experiments |
| `EXTEXP0009` | Hosting experiments |
| `EXTEXP0010` | Object pool experiments |
| `EXTEXP0011` | Document database experiments |
| `EXTEXP0012` | Auto-activation experiments |
| `EXTEXP0013` | HttpLogging middleware experiments |
| `EXTEXP0014` | ASP.NET Core integration testing experiments |
| `EXTEXP0015` | Environmental probes experiments |
| `EXTEXP0016` | Hosting integration testing experiments |
| `EXTEXP0017` | Contextual options experiments |


# LoggerMessage

| Diagnostic ID     | Description |
| :---------------- | :---------- |
| `LOGGEN000` | Don't include log level parameters as templates |
| `LOGGEN001` | Couldn't find a required type definition |
| `LOGGEN002` | Each logging method should use a unique event id |
| `LOGGEN003` | Logging methods must return void |
| `LOGGEN004` | A static logging method must have a parameter that implements the "Microsoft.Extensions.Logging.ILogger" interface |
| `LOGGEN005` | Logging methods must be static |
| `LOGGEN006` | Logging methods must be partial |
| `LOGGEN007` | Logging methods can't be generic |
| `LOGGEN008` | Redundant qualifier in the logging message |
| `LOGGEN009` | Don't include exception parameters as templates in the logging message |
| `LOGGEN010` | The logging template has no corresponding method parameter |
| `LOGGEN011` | A parameter isn't referenced from the logging message |
| `LOGGEN012` | Logging methods can't have a body |
| `LOGGEN013` | A "LogLevel" value must be supplied |
| `LOGGEN014` | Don't include logger parameters as templates |
| `LOGGEN015` | Couldn't find a field of type "Microsoft.Extensions.Logging.ILogger" |
| `LOGGEN016` | Multiple fields of type "Microsoft.Extensions.Logging.ILogger" were found |
| `LOGGEN017` | Can't combine the [LogProperties] or [TagProvider] attributes with data classification attributes |
| `LOGGEN018` | Can't log properties of a parameter or property |
| `LOGGEN019` | Method parameter can't be used to log properties |
| `LOGGEN020` | Logging method parameter type has no public properties to log |
| `LOGGEN021` | Logging method parameter type has cycles in its type hierarchy |
| `LOGGEN022` | Tag provider method not found |
| `LOGGEN023` | Tag provider method is inaccessible |
| `LOGGEN024` | Property provider method has an invalid signature |
| `LOGGEN025` | Logging method parameters can't have "ref" or "out" modifiers |
| `LOGGEN026` | Parameters with a custom tag provider are not subject to redaciton |
| `LOGGEN027` | Multiple logging methods shouldn't use the same event name |
| `LOGGEN028` | Logging method parameter's type has a hidden property |
| `LOGGEN029` | A logging method parameter causes name conflicts |
| `LOGGEN030` | Logging method doesn't log anything |
| `LOGGEN031` | A logging message template starts with "@" |
| `LOGGEN032` | Can only have one of [LogProperties], [TagProvider], and [LogPropertyIgnore] |
| `LOGGEN033` | Method parameter can't be used with a tag provider |
| `LOGGEN034` | Attribute can't be used in this context |
| `LOGGEN035` | The logging method parameter leaks sensitive data |


# Metrics

| Diagnostic ID     | Description |
| :---------------- | :---------- |
| `METGEN000` | Metric method names can't start with an underscore |
| `METGEN001` | Metric method parameter names can't start with an underscore |
| `METGEN002` | Metric names must start with an uppercase alphabetic character |
| `METGEN003` | Multiple metric methods can't use the same metric name |
| `METGEN004` | Metric methods mustn't use any existing type as the return type |
| `METGEN005` | The first parameter should be of type `System.Diagnostics.Metrics.Meter` |
| `METGEN006` | Metric methods must be partial |
| `METGEN007` | Metric methods can't be generic |
| `METGEN008` | Metric methods can't have a body |
| `METGEN009` | Tag names should contain alphanumeric characters and only allowed symbols |
| `METGEN010` | Metric methods must be static |
| `METGEN011` | A strong type object contains duplicate tag names |
| `METGEN012` | A metric class contains an invalid tag name type |
| `METGEN013` | A metric class contains too many tag names |
| `METGEN014` | A metering attribute type argument is invalid |
| `METGEN015` | Metric methods mustn't use any external type as the return type |
| `METGEN016` | Metric methods mustn't use any generic type as the return type |
| `METGEN017` | Gauge is not supported yet |
| `METGEN018` | Xml comment was not parsed correctly |
| `METGEN019` | A metric class has cycles in its type hierarchy |
