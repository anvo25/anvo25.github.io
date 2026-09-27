---
layout: page
permalink: /media/
title: media coverage
description: Press, social media coverage, and mentions of my work.
nav: true
nav_order: 4
_styles: >
  article a { color: var(--global-theme-color) !important; }
  .social-sidebar {
    position: fixed;
    right: 20px;
    top: 80px;
    width: 280px;
    max-height: calc(100vh - 100px);
    overflow-y: auto;
    border-left: 2px solid var(--global-divider-color, #eee);
    padding-left: 1rem;
    font-size: 0.85em;
  }
  .social-sidebar h2 { font-size: 1.4em; margin-bottom: 1rem; }
  details.vn-coverage > summary {
    cursor: pointer;
    color: var(--global-theme-color);
    font-weight: 500;
    list-style: none;
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
  }
  details.vn-coverage > summary::-webkit-details-marker { display: none; }
  details.vn-coverage > summary::before {
    content: "\25B8";
    display: inline-block;
    transition: transform 0.15s ease;
  }
  details.vn-coverage[open] > summary::before { transform: rotate(90deg); }
  details.vn-coverage > summary:hover { text-decoration: underline; }
  details.vn-coverage[open] > summary { margin-bottom: 0.75rem; }
  .social-sidebar blockquote, .social-sidebar iframe { margin-bottom: 1.5rem !important; }
  @media (max-width: 1300px) {
    .social-sidebar {
      position: static;
      width: 100%;
      max-height: none;
      border-left: none;
      border-top: 2px solid var(--global-divider-color, #eee);
      padding-left: 0;
      padding-top: 1rem;
      margin-top: 2rem;
    }
  }
---

## news coverage

<div class="row align-items-start mt-3">
  <div class="col-md-7">
    <div style="position: relative; width: 100%; padding-bottom: 56.25%; height: 0; overflow: hidden;">
      <iframe src="https://www.youtube.com/embed/BkRrO_4OCCc" title="Sky News: AI could be giving US lethal edge in Iran war, but there are dangers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
  </div>
  <div class="col-md-5">
    <h5><a href="https://news.sky.com/story/ai-could-be-giving-us-lethal-edge-in-iran-war-but-there-are-dangers-13514784" target="_blank" style="color: var(--global-theme-color, #0076df);">AI could be giving US lethal edge in Iran war, but there are dangers</a></h5>
    <p><img src="https://www.google.com/s2/favicons?domain=news.sky.com&sz=32" alt="Sky News" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>Sky News</strong></p>
    <p>My paper (<a href="https://vlmsarebiased.github.io" target="_blank">Vision Language Models are Biased</a>) is featured in this Sky News <a href="https://www.youtube.com/watch?v=BkRrO_4OCCc" target="_blank">film</a> and <a href="https://news.sky.com/story/ai-could-be-giving-us-lethal-edge-in-iran-war-but-there-are-dangers-13514784" target="_blank">article</a> discussing the role of AI in modern warfare and its potential dangers.</p>
  </div>
</div>

---

## articles & blog posts

- **KAIST School of Computing** [ICLR 2026 paper reveals memorization bias and limitations in counterfactual reasoning in vision-language models](https://cs.kaist.ac.kr/board/view?bbs_id=news&bbs_sn=11754&menu=83) (2026).
- **Gary Marcus** [GPT-5: Overdue, overhyped and underwhelming](https://garymarcus.substack.com/p/gpt-5-overdue-overhyped-and-underwhelming), cites VLMs are Biased as key evidence for current model limitations.
- **Hacker News** [Front page](https://news.ycombinator.com/item?id=44169413), community discussion of the VLMBias benchmark.
- **LinkedIn** [Post by Alex](https://www.linkedin.com/feed/update/urn:li:share:7360208443477045248), highlights [VLMs are Biased](https://vlmsarebiased.github.io) findings on model failures in counterfactual visual reasoning.

---

## industry usage

<ul>
  <li><img src="https://www.google.com/s2/favicons?domain=kimi.ai&sz=32" alt="" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>Moonshot AI</strong> used <a href="https://vlmsarebiased.github.io" target="_blank">VLMs are Biased</a> as a source benchmark for developing <a href="https://www.kimi.ai/blog/perception-bench" target="_blank">PerceptionBench</a> (2026).</li>
  <li><img src="https://www.google.com/s2/favicons?domain=qwen.ai&sz=32" alt="" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>Alibaba Qwen</strong> used <a href="https://vlmsarebiased.github.io" target="_blank">VLMs are Biased</a> to evaluate <a href="https://qwen.ai/blog?id=qwen3.8" target="_blank">Qwen3.8</a> (2026).</li>
  <li><img src="https://www.google.com/s2/favicons?domain=seed.bytedance.com&sz=32" alt="" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>ByteDance</strong> used <a href="https://vlmsarebiased.github.io" target="_blank">VLMs are Biased</a> to evaluate <a href="https://seed.bytedance.com/en/blog/seed-2-0-official-launch" target="_blank">Seed 2.0</a> (2026) and <a href="https://seed.bytedance.com/en/blog/official-release-of-seed1-8-a-generalized-agentic-model" target="_blank">Seed 1.8</a> (2025).</li>
  <li><img src="https://www.google.com/s2/favicons?domain=deepmind.com&sz=32" alt="" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>Google DeepMind</strong> used <a href="https://vlmsarebiased.github.io" target="_blank">VLMs are Biased</a> to evaluate <a href="https://blog.google/technology/developers/gemini-3-pro-vision" target="_blank">Gemini 3 Pro</a> (2025).</li>
  <li><img src="https://www.google.com/s2/favicons?domain=moondream.ai&sz=32" alt="" style="height: 1.2em; vertical-align: middle; margin-right: 4px;"><strong>Moondream</strong> used examples from <a href="https://vlmsarebiased.github.io" target="_blank">VLMs are Biased</a> to demonstrate reduced counting bias through grounded reasoning in their <a href="https://moondream.ai/blog/moondream-2025-06-21-release" target="_blank">2025-06-21 release</a>.
    <br><img src="/assets/img/moondream example.png" alt="Moondream using VLMs are Biased examples" style="max-width: 100%; margin-top: 0.5rem; border-radius: 6px;"></li>
</ul>

---

## Vietnamese coverage

I had a meaningful and memorable life in Vietnam before going abroad. These are some articles (in Vietnamese) that covered my journey there.

<details class="vn-coverage" markdown="1">
<summary>Show 11 articles</summary>

- 2024: UIT News – [Recipient of Master's Scholarship at Top Korean Research Institute: 'Choosing UIT was my crucial and unforgettable turning point'](https://en.uit.edu.vn/recipient-masters-scholarship-top-korean-research-institute-choosing-uit-was-my-crucial-and-unforgettable-turning-point)
- 2024: UIT Cafe – ["Du học có phải là đích đến cuối cùng?"](https://youtu.be/JmWMcSb6FUk?si=UhfQtuW0RTXfO9CE)
- 2023: Tiền Phong – [Thủ khoa tốt nghiệp toàn diện loại xuất sắc cùng niềm đam mê với khoa học](https://svvn.tienphong.vn/thu-khoa-tot-nghiep-toan-dien-loai-xuat-sac-cung-niem-dam-me-voi-khoa-hoc-post1543034.tpo)
- 2023: Thanh Niên – [Thủ khoa kiên trì với học thuật để "tự do về ý chí và thời gian"](https://thanhnien.vn/thu-khoa-kien-tri-voi-hoc-thuat-de-tu-do-ve-y-chi-va-thoi-gian-185230610152845327.htm)
- 2023: UIT News – [Gặp gỡ chàng sinh viên Khoa học Máy tính với những thành tích tương](https://www.uit.edu.vn/gap-go-chang-sinh-vien-khoa-hoc-may-tinh-voi-nhung-thanh-tich-tuong)
- 2023: Dân Trí – [Lương bèo, bợt nợ ngập đầu – nữ giáo viên muốn đi Úc kiếm tiền tỷ](https://dantri.com.vn/lao-dong-viec-lam/luong-beo-bot-no-ngap-dau-nu-giao-vien-muon-di-uc-kiem-tien-ty-20230404232411805.htm)
- 2023: Tuổi Trẻ – [Lãnh đạo TP.HCM đối thoại với sinh viên tiêu biểu: Mở ra không gian cho cán bộ Gen Z](https://tuoitre.vn/lanh-dao-tp-hcm-doi-thoai-voi-sinh-vien-tieu-bieu-mo-ra-khong-gian-cho-can-bo-gen-z-20230322202149374.htm)
- 2023: VnExpress – [Sinh viên hiến kế để TP.HCM thu hút nhân tài](https://vnexpress.net/sinh-vien-hien-ke-de-tp-hcm-thu-hut-nhan-tai-4584871.html)
- 2022: Tiền Phong – [Hai sinh viên nhận giải thưởng bài báo xuất sắc tại Hội nghị Quốc tế về CNTT và Truyền thông](https://svvn.tienphong.vn/hai-sinh-vien-nhan-giai-thuong-bai-bao-xuat-sac-tai-hoi-nghi-quoc-te-ve-cntt-va-truyen-thong-post1493044.tpo)
- 2022: Tuổi Trẻ – [Ứng dụng AI vào giáo dục lịch sử](https://tuoitre.vn/ung-dung-ai-vao-giao-duc-lich-su-20221004093302994.htm)
- 2018: Đất Mũi – [108 thí sinh tham gia Hội thi Tin học trẻ cấp tỉnh năm 2018](https://baoanhdatmui.vn/108-thi-sinh-tham-gia-hoi-thi-tin-hoc-tre-cap-tinh-nam-2018.html)

</details>

---

<div class="social-sidebar">
  <h2>social media</h2>
  <blockquote class="twitter-tweet" data-dnt="true" data-theme="light">
    <p lang="en" dir="ltr">Oh wow, this VLM benchmark is pure evil, and I love it!</p>
    &mdash; Lucas Beyer (b|16) (@giffmana) <a href="https://twitter.com/giffmana/status/1953931117708669217">August 9, 2025</a>
  </blockquote>
  <blockquote class="twitter-tweet" data-dnt="true" data-theme="light">
    <p lang="en" dir="ltr">This is a really well-done benchmark for evaluating bias in VLMs.</p>
    &mdash; Yoav Goldberg (@yoavgo) <a href="https://twitter.com/yoavgo/status/1954084063892885674">August 10, 2025</a>
  </blockquote>
  <blockquote class="twitter-tweet" data-dnt="true" data-theme="light">
    <p lang="en" dir="ltr">Vision Language Models are Biased</p>
    &mdash; Cohere Labs (@Cohere_Labs) <a href="https://twitter.com/Cohere_Labs/status/1944932457184391442">August 2025</a>
  </blockquote>
</div>

<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
