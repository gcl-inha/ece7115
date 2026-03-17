---
hide:
  - navigation
  - toc
---

# ECE7115 Multimodal VLM (LLM)

<div class="course-subtitle">Inha University · Spring 2026</div>

<div class="course-description" markdown>

This course provides an in-depth study of Large Language Models (LLMs) — the essential foundation for understanding Multimodal Vision-Language Models.
Topics include LLM architectures, training/inference pipelines, GPU systems, and post-training methods such as RLHF and RLVR. (but I will not provide VLM-related topcis, sorry!) <br>
Note: This course is built upon [Stanford CS336](https://cs336.stanford.edu).

**Instructor:** [Namhyuk Ahn](https://nmhkahn.github.io) (School of Electrical and Electronic Engineering, Inha University)

</div>

### Schedule & Lecture Materials
Note: We provide lecture videos in Korean only.
<div class="schedule-table">
<table class="schedule">
  <thead>
    <tr>
      <th class="schedule-date">날짜</th>
      <th class="schedule-desc">내용</th>
      <th class="schedule-slides">Slides</th>
      <th class="schedule-youtube">YouTube</th>
    </tr>
  </thead>
  <tbody>
{% for item in schedule %}
    <tr>
      <td class="schedule-date">{{ item.date }}</td>
{% if item.description_ko is defined and item.description_ko %}
      <td class="schedule-desc">{{ item.description_ko }}</td>
      <td class="schedule-slides"></td>
      <td class="schedule-youtube"></td>
{% else %}
      <td class="schedule-desc">
<span class="lecture-title">{{ item.title_ko }}</span>{% for d in item.details_ko %}<br>- {{ d }}{% endfor %}
      </td>
      <td class="schedule-slides">
{% for s in item.slides %}{% if s.url %}<a href="{{ s.url }}" target="_blank">{{ s.title }}</a>{% endif %}{% if not loop.last %}<br>{% endif %}{% endfor %}
      </td>
      <td class="schedule-youtube">
{% for vid in item.videos %}{% if vid.youtube %}<a href="{{ vid.youtube }}" target="_blank">{{ vid.title }}</a>{% endif %}{% if not loop.last %}<br>{% endif %}{% endfor %}
      </td>
{% endif %}
    </tr>
{% endfor %}
  </tbody>
</table>
</div>
