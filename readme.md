<a name="Modelize"></a>
## Modelize
Transform foreign schema definitions to Sequelize model definitions

**Kind**: global class  
<a name="Modelize.fromJsonSchema"></a>
### Modelize.fromJsonSchema(schemas, schemaId, options) ⇒ <code>Object</code>
Convert a JSON schema into a Sequelize model definition
http://docs.sequelizejs.com/en/latest/docs/models-definition/#definition

**Kind**: static method of <code>[Modelize](#Modelize)</code>  
**Returns**: <code>Object</code> - The model definition to use with `sequelize.define()`.  

| Param | Type | Description |
| --- | --- | --- |
| schemas | <code>Object</code> &#124; <code>Array</code> | A list of json schemas or a single Json schema object. |
| schemaId | <code>string</code> &#124; <code>null</code> | The schema id to build the model definition from. |
| options |  |  |
| options.uniqueFields | <code>Array</code> | a list of fields that have the unique constraint |
| options.mixinFields | <code>Array</code> | a list of properties that are sub-schemas (`object` or `$ref` types) to "flatten" into the model definition. For example, the schema property `"address": { "$ref": "http://example.com/schemas/address" }` will create "address" prefixed fields from the address sub-schema, resulting in model fields like "addressStreetName", "addressStreetNumber", etc. |
| options.customFieldDefinitions | <code>object</code> | Override the generated field definitions with your own. Field name to field definition mapping. |
