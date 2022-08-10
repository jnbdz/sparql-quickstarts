# SPARQL in 11 minutes | Tutorials | SPARQL | Quickstarts

Video: https://www.youtube.com/watch?v=FvGndkpa4K0

## Notes

- Query lang for RDF
- W3C standard
- Lets you describe a collection of three-part statements
    - `emp3    title    "Vice President"`
        - Statements are called: a triple
        - `emp3`: subject, `title`: predicate, `"Vice President": object`
        - You can also see them as: 
            1. entity identifier
            2. attribute name
            3. attribute value
        - URIs: 
            1. http://www.snee.com/hr/emp3
            2. http://www.w3.org/2006/vcard/ns#title (like a job title)
            3. Is just a string
- Subject and predicate -> represented by using URIs (Uniform Resource Identifiers (not like URL))
- The third part (ontology/object) of the triple can also be a URI
    - Lets you connect triples into a graph
- Using the turtle syntax from RDF
    - It makes URIs smaller
    - Using prefix
    - `sn:emp3 vcard:title "Vice President"`
- Any data can be repsented as a collection of triples
- Using the row identifier as the subject and the column as the predicate and the value as the object (imagine a table in a SQL DB)
    - This can give us triples for all the facts in the table
- Using your own property names you can have custome attributes (predicate) (using your domain name)
- RDF makes it easy to mix and match standard vocabularies and customizations
- You can have a multiple values for the same attribute and entity identifier (like in a RDBMS where column + id can have multiple values something you cannot have with a RDBMS)

### Examples
 
```sparql
PREFIX vcard: <http://www.w3.org/2006/vcard/ns#>

SELECT ?person
WHERE
{
  ?person  vcard:family-name "Smith" .
}
```
