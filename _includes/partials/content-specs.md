<table class="usa-table">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Authored?</th>
            <th>Required?</th>
            <th>Content</th>
            <th>Searchable?</th>
            <th>Source</th>
            <th>Notes</th>
        </tr>
    </thead>
    {% for spec in include.content %}
    <tbody>
        <tr>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.name }} </td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.type }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.authored }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.required }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.content }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.searchable }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.source }}</td>
            <td {% if spec.subhead %} style="background-color: #e5a000;" {% endif %} {% if spec.subsubhead %} style="background-color: #005ea2; color: #ffffff" {% endif %}>{{ spec.notes }}</td>
        </tr>
    </tbody>
{% endfor %}
</table>