---
layout: default
title: Open Science in Automotive User Research
---

<style>
table {
    width: 100%;
    table-layout: fixed;
    overflow: auto;
}
th, td {
    padding: 0.5rem 1rem;
    border: 1px solid #ccc;
}
</style>

# Open Science in Automotive User Research

Openness and transparency are critical not only for judging the quality of empirical research, but also for accelerating scientific progress and promoting an inclusive scientific community. This initiative reflects our commitment to driving forward the development of open, user-centered automotive technologies and services, ensuring that knowledge and findings are shared openly to benefit the broader community. Therefore, we provide **practical guidelines** for authors on how to make their research open and transparent, and provide **a platform** for authors to promote the research artifacts they have made available to the broader automotive user research community.

## Why Open Science?

The pursuit of Open Science is essential for several reasons:

- **Accelerating Knowledge Dissemination:** Open Science practices ensure that research findings are shared more broadly and quickly, facilitating faster advancements in the field.
- **Enhancing Collaboration:** By making research data and methodologies openly available, we foster an environment where researchers can easily collaborate, building upon each other's work to push the boundaries of knowledge.
- **Promoting Transparency and Reproducibility:** Open access to research findings and data supports the verification of results, enhancing the credibility and reliability of research within our community.


## Toward Open Science

**Every step** toward greater transparency in research is valuable, contributing incrementally to the overall integrity and reproducibility of scientific work. It's important to recognize and celebrate each step taken, even if complete openness is not immediately achieved. Here are three levels of engagement with open science practices:

- **Level 1**:
  - **Document methods and results**: Even if data cannot be shared, detailed documentation of research methods and results can be invaluable. If you can't share the raw data, maybe you can share aggregated data or the statistics of the data.
  - **Acknowledge limitations**: Clearly state any restrictions on data sharing and transparency, explaining the reasons behind them.

- **Level 2**:
  - **Share data when possible**: When permissible, share data in a trusted repository, ensuring it is de-identified and secure.
  - **Use open-access platforms**: Publish findings open-access and on [FAIR](https://www.go-fair.org/fair-principles/) (findable, accessible, interoperable, and reusable) platforms to make the research accessible to a broader audience.

- **Level 3**:
  - **Full data and code availability**: Share all research data, code, and materials necessary to replicate the study and reproduce the results.
  - **Engage in pre-registration**: Register study protocols in advance to enhance the credibility of the research.




## Practical Tips for Authors

Following the guidelines we shared for the [AutomotiveUI '24 conference](https://www.auto-ui.org/24/authors/open-science/), here are practical tips to incorporate Open Science into your research workflow:

### Data Sharing and Management

There are many places where we can publish open access artifacts. It is good practice to keep your data on a [FAIR](https://www.go-fair.org/fair-principles/)  platform/repository. Here are some examples (updated June 2024):

1. **[ACM Digital Library](https://dl.acm.org)** (FAIR): AutoUI is an ACM conference, and the platform allows the sharing of (small) supplementary material with the publication.
2. **[OSF](https://osf.io)** (FAIR): Allows to make repos anonymous for review, which can be handy for the submission process. It is a ‘swiss knife’ for publishing artifacts in open access, and the platform allows a great level of flexibility. File versioning is straightforward, and OSF also allows you to pre-register your study. It is also easy to make your material anonymous for the review process.
3. **[Zenodo](https://zenodo.org)** (FAIR): Data is stored at CERN, which is reliable. It is becoming a common place to share data, which may make it user-friendly. They accept up to 50GB per dataset with an option to have multiple datasets.
4. **[GitHub](https://github.com)** (**not** FAIR; see [here](https://fairdataforum.org/t/can-github-be-considered-a-fair-repository/410/2)) Everyone knows how to navigate around a repo on GitHub, which can be an advantage for outreach. But it is not FAIR as no **globally unique** and **persistent** identifier is created. What can be practiced is to provide a link to the active project in the manuscript, and then still upload materials to a FAIR platform for reproducibility.
5. **[4TU.ResearchData](https://data.4tu.nl)** (FAIR): Local storage for the technical universities of the Netherlands. They do quite a good job of making the management of datasets easy. Likely, there is a similar portal in your institution/country.



### Open Access Publications

- **Choose Open Publishers:** When publishing your findings, opt for conferences and journals that offer open access, making your research available to all. Avoid [Predatory Journals](https://beallslist.net/).
- **Preprints:** Consider posting preprints of your research to platforms such as [arXiv](https://arxiv.org/), [bioRxiv](https://www.biorxiv.org/), or [OSF](https://www.osf.io/preprints). This is a good way of sharing your results either prior to publication or in case you cannot or do not want to pay the open access fees of publishers.

### Transparency in Methodology

- **Code Sharing:** Use [FAIR](https://www.go-fair.org/fair-principles/) platforms/repositories (see above) to share the code used in your research, including analysis scripts and software developed as part of your work.
- **Detailed Documentation:** Ensure that your methodologies are thoroughly documented and shared, allowing others to replicate or build upon your work.

## Openly Available Research Artifacts

Here, we provide a dynamically updated table of related works, categorized by the criteria datasets, simulation software and models to facilitate easy access to a wealth of resources that can support your research and inspire your Open Science endeavors.

**We encourage authors of papers with openly available materials who want to link their work on this site to create a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)  on [GitHub](https://github.com/AutoUI-Open-Data-Initiative/autoui-open-data-initiative.github.io) to add their work**. 
Add your work here: [Related Works CSV](https://raw.githubusercontent.com/AutoUI-Open-Data-Initiative/autoui-open-data-initiative.github.io/master/_data/related_works.csv).
The category must be one of [Dataset, Software, Model]. Please make sure your pull requests complies with the format.
We will check the entry and approve it as soon as possible. 





<!-- Include DataTables CSS -->
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.11.5/css/jquery.dataTables.css">

<style>
  table.dataTable tbody td {
    white-space: nowrap;
    overflow-x: auto;
    max-width: 0;
    cursor: pointer;
    font-size: 0.9em; /* Slightly reduced font size */
  }

  table.dataTable thead th {
    font-size: 0.9em; /* Reduce header font size to match body */
  }

  .dataTables_wrapper {
    width: 100%;
    overflow-x: auto;
  }
</style>

<!-- Table Structure -->
{% assign categories = site.data.related_works | group_by: "Category" %}
{% for category in categories %}
  <h3>{{ category.name }}</h3>
  <table id="table-{{ category.name | slugify }}" class="display" style="width:100%">
    <thead>
      <tr>
        <th style="width: 45%">Title</th>
        <th style="width: 30%">Author</th>
        <th style="width: 10%">Year</th>
        <th style="width: 15%">Resources</th>
      </tr>
    </thead>
    <tbody>
      {% for row in category.items %}
        <tr>
          <td><a href="{{ row["Paper-Link"] }}">{{ row.Title }}</a></td>
          <td>{{ row.Author }}</td>
          <td>{{ row.Year }}</td>
          <td>
            {% if row["Repo-Link"] %}
              <a href="{{ row["Repo-Link"] }}">Link</a>
            {% endif %}
          </td>
        </tr>
      {% endfor %}
    </tbody>
  </table>
{% endfor %}

<!-- Include jQuery and DataTables JS -->
<script type="text/javascript" charset="utf8" src="https://code.jquery.com/jquery-3.5.1.js"></script>
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.11.5/js/jquery.dataTables.js"></script>

<!-- Initialize DataTables -->
<script>
  $(document).ready(function() {
    {% for category in categories %}
      $('#table-{{ category.name | slugify }}').DataTable({
        "autoWidth": false,
        "columnDefs": [
          { "width": "45%", "targets": 0 },
          { "width": "30%", "targets": 1 },
          { "width": "10%", "targets": 2 },
          { "width": "15%", "targets": 3 }
        ]
      });
    {% endfor %}
  });
</script>




## Paper and Workshop

For more information on the current state of the art and the motivators and barriers to open science in the automotive user research community, see the [paper](https://osf.io/tmkc2) or its materials published on [OSF](https://osf.io/zdpek/). If you find this information useful, please consider citing it:
```
@inproceedings{ebel2024changing,
  title={Changing Lanes Toward Open Science: Openness and Transparency in Automotive User Research},
  author={Ebel, Patrick and Bazilinskyy, Pavlo and Colley, Mark and Goodridge, Courtney and Hock, Philipp and Janssen, Christian P. and Sandhaus, Hauke and Srinivasan, Aravinda Ramakrishnan and Wintersberger, Philipp},
  booktitle={16th International Conference on Automotive User Interfaces and Interactive Vehicular Applications (AutomotiveUI '24)},
  pages={17},
  year={2024},
  address={Stanford, California, USA},
  month={sep},
  publisher={ACM},
  location={New York, NY, USA},
  note={Conditionally accepted}
}
```

Also see the 2023 workshop [website](https://autouimodelingws.jimdosite.com/) for more information.







