<table class="usa-table">
    <thead>
        <tr>
            <td>Label</td>
            <td>Required?</td>
            <td>Field Type</td>
            <td>Field</td>
            <td>Error</td>
        </tr>
    </thead>
    {% for spec in include.content %}
    <tbody>
        <tr>
            <td>{{ spec.name }} </td>
            <td>{{ spec.required }}</td>
            <td>{{ spec.field }} </td>
            <td>{{ spec.content }}</td>
            <td>{{ spec.error }}</td>
        </tr>
    </tbody>
    {% endfor %}
</table>