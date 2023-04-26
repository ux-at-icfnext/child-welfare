<label class="usa-button dd">
    <div class="dropdown-button">
        <i class="fas fa-download"></i>
        download
    </div>
    <div class="dd-icon">
        <i class="fa-solid fa-chevron-down"></i>
    </div>
    <input type="checkbox" class="dropdown-input">
    <ul class="dropdown-menu">
        {% for item in site.data.contentful.spaces.example.publicationResource[0].download_file_size %}
            <li>{{item}}</li>
        {% endfor %}
    </ul>
</label>