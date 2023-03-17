<label class="usa-button dd">
    <div class="dropdown-button">
        <i class="fas fa-download"></i>
        Download
    </div>
    <div class="dd-icon">
        <img src="/assets/icons/expand_more_white.svg" height="32px" width="auto">
    </div>
    <input type="checkbox" class="dropdown-input">
    <ul class="dropdown-menu">
    {% for item in site.data.contentful.spaces.example.publicationResource[0].download_file_size %}
        <li>{{item}}</li>
    {% endfor %}
    </ul>
</label>