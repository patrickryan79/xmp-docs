# <Label>

<a name="top"></a>

[Syntax](#syntax) [Remarks](#remarks) [Example](#example)

The Label tag renders as a static text at run-time.

<a name="syntax"></a>

## Syntax

<div>`<Label`  
`    ID="_string_"`  
`    For="_string_"`  
`    Text="_string_"`  
`    CssClass="_string_"`  
`    Visible="**True**|False"`  
`/> `</div>

 <a name="remarks"></a>

## Remarks

The Label tag provides the ability to offer better accessibility to your users by using the "For" attribute to identify a form control for which the label provides the caption. This makes it much easier for screen reader applications to understand your form. When supplying text for the Label, you can either place it in the _Text_ attribute or you can place it between the opening `<Label>` and closing `</Label>` tags.

*   **ID**: Name, consisting of letters and numbers, beginning with a letter, that uniquely identifies the control within the form.  

*   **For**: The attribute linking the label to a form control for which the label provides the caption.  

*   **Text**: The attribute used to display text.  

*   **CssClass**: Name of the Cascading Style Sheets (CSS) class used to style this control.  

*   **Visible**: Determines if the control is visible (true) or hidden (false). Default set to "True".

[Back to top](#top)<a name="example"></a>

## Example

<div>`<AddForm>`  
`  ...`  
` <table>`  
`    <tr>`  
`      <td>`  
`        <Label Id="lblFirstName" For="txtFirstName" Text="First Name" />`  
`        <TextBox Id="txtFirstName" DataField="FirstName" DataType="string" />`  
`      </td>`  
`    </tr>`  
`    <tr>`  
`       <td>`  
`         <Label Id="lblLastName" For="txtLastName" Text="Last Name" />`  
`         <TextBox Id="txtLastName" DataField="LastName" DataType="string" />`  
`       </td>`  
`    </tr>`  
`    <tr>`  
`      <td colspan="2">`  
`        <AddButton Text="Add" /> <CancelButton Text="Cancel" />`  
`       </td>`  
`    </tr>`  
`  </table>`  
`</AddForm>`</div>

[Back to top](#top)