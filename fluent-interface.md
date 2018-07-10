# Fluent Interface

In software engineering, a fluent interface (as first coined by Eric Evans and Martin Fowler) or a fluent API is a method for designing object oriented APIs based extensively on *method chaining* with the goal of making the readability of the source code close to that of ordinary written prose, essentially creating a domain-specific language within the interface.

For example,

C# uses fluent programming extensively in LINQ to build queries using the standard query operators. The implementation is based on extension methods.

```C#
var translations = new Dictionary<string, string>
                   {
                       {"cat", "chat"},
                       {"dog", "chien"},
                       {"fish", "poisson"},
                       {"bird", "oiseau"}
                   };

// Find translations for English words containing the letter "a",
// sorted by length and displayed in uppercase
IEnumerable<string> query = translations
	.Where   (t => t.Key.Contains("a"))
	.OrderBy (t => t.Value.Length)
	.Select  (t => t.Value.ToUpper());
  ```
  
  ## Further reading
  * [Wikipedia page on Fluent interface](https://en.wikipedia.org/wiki/Fluent_interface)
