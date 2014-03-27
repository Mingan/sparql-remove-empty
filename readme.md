General SPARQL query for removing empty and pseudo-empty string literals. Intended as a configuration for [UnifiedViews](https://github.com/UnifiedViews/Core)/[ODCS](https://github.com/mff-uk/ODCS) SPARQL Transformer DPU.

Default configuration removes all empty literals regardles of language tag. Optional filtering by predicate is prepared, as well as filtering by subject class. Any other graph pattern can be added but you should take care to DELETE the correct triple. Default behavior uses exact match of string value (without langauge tag), if you need regular expressions you have to change the last filter or prepare data first (see below) 

This query is intended to run after [trimming query](https://github.com/Mingan/sparql-trimming) which removes all whitespaces from ends of strings.

If data contains dummy values you might want to use [literal normalizer](https://github.com/Mingan/literal-normalizer) first to change all alternatives (eg. "unknown", "N/A", "...") to single value (eg. "") and then remove that with this query. Literal normalizer supports regular expressions.