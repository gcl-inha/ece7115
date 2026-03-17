---
hide:
  - navigation
  - toc
---

# ECE7115 Multimodal VLM (LLM)

<div class="course-subtitle">인하대학교 · 2026년 봄학기</div>

<div class="course-description" markdown>

본 강의는 Multimodal VLM을 이해하기 위한 핵심 기반인 대규모 언어 모델(Large Language Model; LLM)을 심도 있게 다룹니다.
Transformer부터 최신 LLM 모델 아키텍처, 학습/추론 파이프라인, GPU 시스템, RL 기반 사후 학습까지 LLM의 기초부터 최신 기술을 학습합니다. (강의 이름과 다르게 VLM 내용은 다루지 않습니다!) <br>
참고: 본 강의는 [Stanford CS336](https://cs336.stanford.edu)을 기반으로 구성되었습니다.

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
