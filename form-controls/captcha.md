# <Captcha>

<a name="top"></a>

[Syntax](#syntax) [Remarks](#remarks) [Example](#example)

The Captcha tag renders as a CAPTCHA control at run time.

**NOTE**: Due to a limitation in the underlying DNN CAPTCHA control, this tag can only be used in the FormView module.

<a name="syntax"></a>

## Syntax

<div>`<Captcha``  
    BackColor="_color name_|#dddddd"  
    BackgroundColor="_color name_|#dddddd"  
    BackgroundImage="_url_"  
    BorderColor="_color name_|#dddddd"  
    BorderStyle="**NotSet**|None|Dotted|Dashed|Solid|Double|Groove|Ridge| Inset|Outset"  
    BorderWidth="_size_"  
    CaptchaChars="_string_"  
    CaptchaHeight="_size_"  
    CaptchaLength="_integer_"  
    CaptchaWidth="_size_"  
    CssClass="_string_"  
`    ErrorMessage="_string_"`  
`    ErrorStyle-BackColor="_color name_|#dddddd"  
    ErrorStyle-BorderColor="_color name_|#dddddd"  
    ErrorStyle-BorderStyle="**NotSet**|None|Dotted|Dashed|Solid|Double|Groove|Ridge|Inset|OutSet"  
    ErrorStyle-BorderWidth="_size_"  
    ErrorStyle-Font-Bold="True|**False**"  
    ErrorStyle-Font-Italic="True|**False**"  
    ErrorStyle-Font-Names="_string_"  
    ErrorStyle-Font-Overline="True|**False**"  
    ErrorStyle-Font-Size="_string_|Smaller|Larger|XX-Small|X-Small|Small|Medium| Large|X-Large|XX-Large"  
    ErrorStyle-Font-Strikeout="True|**False**"  
    ErrorStyle-Font-Underline="True|**False**"  
    ErrorStyle-ForeColor="_color name_|#dddddd"  
    Expiration="_integer_"  
`    Font-Bold="True|**False**"  
    Font-Italic="True|**False**"  
    Font-Names="_string_"  
    Font-Overline="True|**False**"  
    Font-Size="_string_|Smaller|Larger|XX-Small|X-Small|Small|Medium| Large|X-Large|XX-Large"  
    Font-Strikeout="True|**False**"  
    Font-Underline="True|**False**"  
    ForeColor="_color name_|#dddddd"  
    Height="_size_"  
    ID="_string_"  
    Text="_string_"  
    Width="_size_"  
``/> `</div>

 <a name="remarks"></a>

## Remarks

If your forms are available to the public, chances are you'll get web 'bots filling in those forms with bogus information. To help protect against this, you can add a CAPTCHA control to your form. The control attempts to prove the user is an actual human by asking them to view a series of characters and typing those characters into a box for verification. The characters are rendered as an image and are skewed and obfuscated so that (hopefully) only a human could read them. While it is no guarantee your forms won't get spammed, the control typically reduces the frequency of those attacks.

*   **BackColor**: Color of the background of the control.  

*   **BackgroundColor**: Gets and sets the background color.  

*   **BackgroundImage**: A URL to an image file to use as the background on which the characters will be placed. (optional).  

*   **BorderColor**: Color of the border around the control.  

*   **BorderStyle**: Style of the border around the control.  

*   **BorderWidth**: Width of the border around the control, specified in [units.  

    ](units.html)
*   **CaptchaChars**: If you wish to specify your own characters that will be used to make up the code the user must type, you can specify them in this property.  

*   **CaptchaHeight**: The height of the area in which the characters will be displayed.  

*   **CaptchaLength**: The number of characters to use for the code.  

*   **CaptchaWidth**: The width of the area in which the characters will be displayed.  

*   **CssClass**: Name of the Cascading Style Sheets (CSS) class used to style this control.  

*   **ErrorMessage**: The message to display to the user if Captcha validation failed.  

*   **ErrorStyle**: The style to use for displaying the error message. ErrorStyle is specified using the following syntax: ErrorStyle-styleAttributeName where 'styleAttributeName' is the name of the style attribute such as ForeColor or Font-Bold. See the syntax section above for more.  

*   **Expiration**: Gets and sets the Expiration time in seconds.  

*   **Font Properties**: A series of attributes such as font-bold, font-size, etc. that allow you to control how the text in the control is displayed. [More  

    ](fontproperties.html)
*   **ForeColor**: Sets the foreground color (typically the color of the text) of the control.  

*   **Height**: Height of the control, specified in [units](units.html).  

*   **ID**: Name, consisting of letters and numbers, beginning with a letter, that uniquely identifies the control within the form.  

*   **Text**: The caption to display.  

*   **Width**: Width of the control in [units](units.html).  

[Back to top](#top)<a name="example"></a>

## Example

<div xmlns="">`<AddForm>`  
`  ...`  
`  <table>`  
`    <tr>`  
`      <td>`  
`        <Label For="txtFirstName" Text="First Name" />`  
`        <Textbox id="txtFirstName" DataField="FirstName" DataType="string" />`  
`      </td>`  
`    </tr>`  
`    <tr>`  
`      <td>`  
`        <Label For="txtLastName" Text="First Name" />`  
`        <Textbox Id="txtLastName" DataField="LastName" DataType="string" />`  
`       </td>`  
`    </tr>  
    <tr>  
      <td>  
<span style="color: #ff0000;"><Captcha CaptchaLength="5" /></span>  
      </td>  
    </tr>`  
`    <tr>`  
`      <td colspan="2">`  
`        <AddbButton Text="Add"/>&nbsp; <CancelButton Text="Cancel"/>`  
`      </td>`  
`    </tr>`  
`  </table>`</div>

<div xmlns="">  
`</AddForm>`</div>

[Back to top](#top)