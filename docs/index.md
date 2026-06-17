---
hide:
  - navigation
  - toc
---

# Large Language Models Course

<div class="course-subtitle">인하대학교 · 2026년 봄학기</div>
<div class="course-description" markdown>
본 강의는 대규모 언어 모델(Large Language Model; LLM)의 전반을 이해하는 것을 목표로 합니다. Transformer 및 LLM의 아키텍쳐부터 LLM의 학습과 인퍼런스, GPU 시스템 및 RL 기반 post-training까지 LLM을 이해하는 데 필요한 주요 내용을 학습합니다.<br>
참고: 인하대학교에서 개설된 공식 강의명은 Multimodal VLM (ECE7115)이지만, 실제 강의 내용은 LLM을 중심으로 구성되어 있습니다.<br>
**강의자:** [안남혁](https://nmhkahn.github.io) (인하대학교 전기전자공학부)
</div>

### 강의 스케쥴 & 자료
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
