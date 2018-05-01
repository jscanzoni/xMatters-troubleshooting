# xMatters Troubleshooting Tips
I'm going to keep building this out as I work with xMatters more

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

# Pre-Requisites
* xMatters account - If you don't have one, [get one](https://www.xmatters.com)!

# Testing
As always, make sure to develop and test on a non-production environment. Running this code unmodified in production could have unintended consequences.

# Troubleshooting

## Integration Builder
When working in the [Integration Builder](https://help.xmatters.com/OnDemand/xmodwelcome/integrationbuilder/build-integrations.htm), using `console.log(variable);` is helpful when you want to see is something is being set. To get the output of a JSON object, such as the `callback` being passed into your integration, you'll want to use the following to output and format it into a readable JSON format.
```javascript
console.log(JSON.stringify(callback, null, 2));
```
## Python
Add this code anywhere you need to see the raw response from the [API](https://help.xmatters.com/xmAPI/) -- great for troubleshooting connection or data formatting issues.
```python
print '\n\n\n'+str(response.json())+'\n\n\n'
print str(data_string)+'\n\n\n'
```
