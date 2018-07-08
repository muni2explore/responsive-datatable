# Responsive Datatable
```html
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Class</th>
            <th>Native</th>
            <th>University</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Jagan</td>
            <td>A</td>
            <td>Villlupuram</td>
            <td class="fourth">Anna University</td>
        </tr>
        <tr>
            <td>Muni</td>
            <td>A</td>
            <td>Krishnagiri</td>
            <td class="fourth">Anna University</td>
        </tr>

    </tbody>
</table>
```
Styles

```css
table {
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
}

td, th {
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
    width: 25%;
}

tr:nth-child(even) {
    background-color: #dddddd;
}

@media screen and (max-width:720px) {
    thead{
        display: none;
    }
    td:nth-of-type(1):before { content: "Name: "; }
td:nth-of-type(2):before { content: "Class: "; }
td:nth-of-type(3):before { content: "Native: "; }
    td:nth-of-type(4):before { content: "University: "; }

    td{
        width: 50%;
        display: table-cell;
        padding: 10px 20px;
        border-right: 1px solid #393939;
        vertical-align: middle;
        border-collapse: collapse;
        float:left;
        box-sizing:border-box; 
    }

    td:nth-child(3n) {
        display: block;
    }
    tr {
  display: block;
    }

    .fourth{
        margin-bottom: 20px;
    }
}

@media screen and (max-width:360px) {
    td{width:100%;}
    tr, td{
        display: block;
        background: red;
    }
}
```
