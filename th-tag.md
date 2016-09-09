# &lt;th&gt;

The *table header* cell, **&lt;th&gt;**, contains header information that describes table cells and can only be a child of a &lt;tr&gt; element. It has a default text value of bold and centered. <!--The standard cell (`td`) is the second type of cell used inside of an HTML table it contains data relevant to its header.
-->  
## Atrributes

The &lt;th&gt; tag contains four unique attributes.

- **colspan**: This attribute will set the number of columns a header cell should span. It will contain a non-negative integer and has a default value of 1 and a max value of 1000.
	
	Syntax: `<th colspan="number">`

- **rowspan**: This attribute will set the number of rows a header cell should span. It will contain a non-negative integer and has a default value of 1 and a max value of 65534.
	
	Syntax: `<th rowspan="number">`

- **scope**: This attribute is used when the &lt;th&gt; tag is not in the first row or column. It creates a relationship between the &lt;th&gt; tag and table cells by identifying the &lt;th&gt; tag as a row (row), a column (col), a group of rows (rowgroup) or a group of columns (colgroup). If you have a complex table, use the `headers` attribute to identify relationships.

	Syntax: `<th scope="col|row|colgroup|rowgroup">`

- **headers**: This attribute creates a relationship between a cell and one or more &lt;th&gt; tags. Each &lt;th&gt; tag must contain an `id` attribute. The cell's `headers` attribute will contain a space-separated string value of all &lt;th&gt; tag ids related to it. The `headers` attribute is not useful when using tables for layouts.
	
	Syntax: `<th headers="th_id">`

## Example 1

In this example we use the `colspan` attribute to span two columns.

 <table>
   <tr>
     <th colspan="2">Quiz</th>
   </tr>
   <tr>
     <td>Question 1</td>
     <td>yes</td>
   </tr>
   <tr>
     <td>Question 2</td>
     <td>no</td>
   </tr>
   <tr>
     <td>Question 3</td>
     <td>yes</td>
   </tr>
 </table>

The code:

```
 <table>
   <tr>
     <th colspan="2">Quiz</th>
   </tr>
   <tr>
     <td>Question 1</td>
     <td>yes</td>
   </tr>
   <tr>
     <td>Question 2</td>
     <td>no</td>
   </tr>
   <tr>
     <td>Question 3</td>
     <td>yes</td>
   </tr>
 </table>
```

## Example 2: rowspan attribute

In this example we use the `rowspan` attribute to extend the rows.

<table>
  <tr>
    <th rowspan="2">Question1</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
  <tr>
    <th rowspan="2">Question2</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
  <tr>
    <th rowspan="2">Question3</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
</table>

The code:
	
```
 <table>
  <tr>
    <th rowspan="2">Question1</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
  <tr>
    <th rowspan="2">Question2</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
  <tr>
    <th rowspan="2">Question3</th>
    <td>yes</td>
  </tr>
  <tr>
    <td>no</td>
  </tr>
</table>	
```

## Example 3: scope attribute

In this example we use the `scope` attribute in the second column and first row to identify their relationship to the table data. The first column contains numbers for the rows.


<table>
  <tr>
    <td></td>
    <th scope="col">Employee</th>
    <th scope="col">Phone#</th>
    <th scope="col">City</th>
    <th scope="col">Time Zone</th>
  </tr><tr>
    <td>1.</td>
    <th scope="row">Scott Chen</th>
    <td>111-111-1111</td>
    <td>Pittsburgh</td>
    <td>EDT</td>
  </tr><tr>
    <td>2.</td>
    <th scope="row">Gabriel Ortiz</th>
    <td>333-333-3333</td>
    <td>Baltimore</td>
    <td>EDT</td>
  </tr><tr>
    <td>3.</td>
    <th scope="row">Peter Clark</th>
    <td>555-555-5555</td>
    <td>Houston</td>
    <td>CDT</td>
  </tr>
</table> 

The code:

```
 <table>
  <caption>Contact Information</caption>
  <tr>
    <td></td>
    <th scope="col">Employee</th>
    <th scope="col">Phone#</th>
    <th scope="col">City</th>
    <th scope="col">Time Zone</th>
  </tr><tr>
    <td>1.</td>
    <th scope="row">Scott Chen</th>
    <td>111-111-1111</td>
    <td>Pittsburgh</td>
    <td>EDT</td>
  </tr><tr>
    <td>2.</td>
    <th scope="row">Gabriel Ortiz</th>
    <td>333-333-3333</td>
    <td>Baltimore</td>
    <td>EDT</td>
  </tr><tr>
    <td>3.</td>
    <th scope="row">Peter Clark</th>
    <td>555-555-5555</td>
    <td>Houston</td>
    <td>CDT</td>
  </tr>
</table>
```

## Example 4:

In this example we use the `headers` attribute to identify the relationship between &lt;th&gt; tags and their cells.

```
	<table>
  		<tr>
    		<th id="question" rowspan="2">Question</th>
    		<th id="women" colspan="2">Women</th>
    		<th id="men" colspan="2">Men</th>
  		</tr>
  		<tr>
    		<th id="w-yes" headers="women">yes</th>
    		<th id="w-no" headers="women">no</th>
    		<th id="m-yes" headers="men">yes</th>
    		<th id="m-no" headers="men">no</th>
  		</tr>
  		<tr>
  			<th id="q-1" headers="question">Question 1</th>
  			<td headers="q1 women w-yes">15%</td>
  			<td headers="q1 women w-no">85%</td>
  			<td headers="q1 men m-yes">30%</td>
  			<td headers="q1 men m-no">70%</td>
  		</tr>
  		<tr>
  			<th id="q-2" headers="question">Question 2</th>
  			<td headers="q1 women w-yes">40%</td>
  			<td headers="q1 women w-no">60%</td>
  			<td headers="q1 men m-yes">51%</td>
  			<td headers="q1 men m-no">49%</td>
  		</tr>
  		<tr>
  			<th id="q-3" headers="question">Question 3</th>
  			<td headers="q1 women w-yes">80%</td>
  			<td headers="q1 women w-no">20%</td>
  			<td headers="q1 men m-yes">75%</td>
  			<td headers="q1 men m-no">25%</td>
  		</tr>
  		<tr>
  			<th id="q-4" hearders="question">Question 4</th>
  			<td headers="q1 women w-yes">15%</td>
  			<td headers="q1 women w-no">85%</td>
  			<td headers="q1 men m-yes">30%</td>
  			<td headers="q1 men m-no">70%</td>
  		</tr>
	</table>

````

<table>
  		<tr>
    		<th id="question" rowspan="2">Question</th>
    		<th id="women" colspan="2">Women</th>
    		<th id="men" colspan="2">Men</th>
  		</tr>
  		<tr>
    		<th id="w-yes" headers="women">yes</th>
    		<th id="w-no" headers="women">no</th>
    		<th id="m-yes" headers="men">yes</th>
    		<th id="m-no" headers="men">no</th>
  		</tr>
  		<tr>
  			<th id="q-1" headers="question">Question 1</th>
  			<td headers="q1 women w-yes">15%</td>
  			<td headers="q1 women w-no">85%</td>
  			<td headers="q1 men m-yes">30%</td>
  			<td headers="q1 men m-no">70%</td>
  		</tr>
  		<tr>
  			<th id="q-2" headers="question">Question 2</th>
  			<td headers="q1 women w-yes">40%</td>
  			<td headers="q1 women w-no">60%</td>
  			<td headers="q1 men m-yes">51%</td>
  			<td headers="q1 men m-no">49%</td>
  		</tr>
  		<tr>
  			<th id="q-3" headers="question">Question 3</th>
  			<td headers="q1 women w-yes">80%</td>
  			<td headers="q1 women w-no">20%</td>
  			<td headers="q1 men m-yes">75%</td>
  			<td headers="q1 men m-no">25%</td>
  		</tr>
  		<tr>
  			<th id="q-4" hearders="question">Question 4</th>
  			<td headers="q1 women w-yes">15%</td>
  			<td headers="q1 women w-no">85%</td>
  			<td headers="q1 men m-yes">30%</td>
  			<td headers="q1 men m-no">70%</td>
  		</tr>
	</table>

## Browser support

The `th` element works in all modern browsers.


| Chrome | Firefox | IE / Edge | Opera | Safari |
| :----: | :----: | :----: | :----: | :----: |
| yes | yes | yes | yes | yes |


## Special Notes

The following attributes are deprecated and should not be used.

| Attribute | Information |
|:-------:|:---------|
| abbr| Do not use, it is obsolete and not supported in the latest standard |
| align | Use the CSS `text-align property` instead |
| axis | Use the `scope` attribute attribute instead |
| bgcolor | Use the CSS property `background-color` instead |
| char | Do not use, it is obsolete and not supported in the latest standard | 
| charoff | Do not use, it is obsolete and not supported in the latest standard |
| height | USe the CSS `height` property instead |
| nowrap | Use the CSS `white-space` property set to `nowrap` instead |
| sorted | If you need to sort a table use JavaScript |
| valign | Use the CSS `vertical-align` property instead |
| width | Use the CSS `width` property instead |

