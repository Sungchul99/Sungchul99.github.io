---
title: CV
permalink: /cv/
redirect_from:
  - /resume
---

{% assign cv_pdf = site.static_files | where: "path", "/files/cv.pdf" | first %}
{% if cv_pdf %}
<div class="cv-actions">
  <a class="btn" href="{{ '/files/cv.pdf' | relative_url }}" target="_blank" rel="noopener">Open PDF</a>
  <a class="btn" href="{{ '/files/cv.pdf' | relative_url }}" download>Download</a>
</div>
<object class="cv-embed" data="{{ '/files/cv.pdf' | relative_url }}" type="application/pdf">
  <p>Your browser cannot display the PDF here. <a href="{{ '/files/cv.pdf' | relative_url }}">Open the CV</a> instead.</p>
</object>
{% else %}
<p>CV will be available soon.</p>
{% endif %}
