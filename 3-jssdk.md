
# JavaScript SDK Reference

For your UI Application, you can use JavaScript SDK to handle edge cases and to develop custom blocks. 

```javascript
function execute(controller){
	const {inputs,node} = controller;
	const {config} = node;
}
```

## Attributes in 'controller'

#### blueprint
#### mainVue
#### uiId
#### uiContainer
#### inputs

## Attributes in 'input'

#### scope
#### current
#### rootScope
#### props
#### path
#### query

## Attributes in 'node'

#### urn
#### config

## SDK Methods

#### getTemplatedValue()
#### getTemplatedAndConvertedValue()
#### setResponse()
