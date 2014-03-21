General SPARQL query for removing empty and pseudo-empty string literals. Intended as a configuration for [UnifiedViews](https://github.com/UnifiedViews/Core)/[ODCS](https://github.com/mff-uk/ODCS) SPARQL Transformer DPU.

Default configuration removes all empty literals. Alternative fitlering by predicate is prepared, as well as optional fitler by subject class.

Regular expression can be modified to accomodate any pseudo-empty string (eg. ":") that should be removed.

This query is intended to run after [trimming query](https://github.com/Mingan/sparql-trimming), if not regexp should be modified to accomodate possible whitespace.