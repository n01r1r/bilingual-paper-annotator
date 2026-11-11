# HTML assembly contract

Copy [paper-reader.html](../assets/paper-reader.html) into the requested deliverable. Replace all `@@...@@` slots and save the result as UTF-8. Keep the CSS and JavaScript inline. Use installed fonts through the template's fallback stacks. Embed source figures as data URLs where needed. Render equations with inline MathML or an embedded source rendering when needed to preserve notation offline. Use external URLs only as optional outbound references. The reader and source content must work with network access disabled.

## Header and sections

- Replace both `@@TITLE@@` slots with the escaped original title. At `@@COURSE@@`, insert a `<p class="course">` with the supplied course information or leave the slot empty when none was supplied.
- At `@@SECTION_LINKS@@`, add a link for every major source section in source order. Match its fragment exactly to the section's unique ID. The template includes the overview link. Use short navigation labels where helpful and preserve full original headings in the paper body.
- At `@@PAPER_SECTIONS@@`, add the source sections with their original hierarchy. Use nested headings or sections for subsections. If a subsection appears in the navigation, include its unique fragment and keep it in document order.

```html
<a href="#methods">
  <span class="label-en" lang="en">Methods</span>
  <span class="label-ko" lang="ko">연구 방법</span>
</a>
```

```html
<section class="paper-section" id="methods">
  <h2><span lang="en">Methods</span>
      <span class="heading-ko" lang="ko">연구 방법</span></h2>
  <!-- Insert paragraph pairs and source objects in their original order. -->
</section>
```

## Paragraph pairs

Use one `.paragraph-pair` per source paragraph. Keep the source block first and the annotation second. The grid aligns both columns on desktop. On mobile, the DOM order places the annotation after the English paragraph and its translation.

```html
<div class="paragraph-pair" id="methods-p1">
  <div class="source">
    <div class="source-en" lang="en">
      <p>Exact English text with a <mark class="method">method passage</mark>.</p>
    </div>
    <div class="source-ko" lang="ko">
      <p>해당 문단의 전체 번역.</p>
    </div>
  </div>
  <aside class="annotation method">
    <dl class="analysis-en" lang="en">
      <dt>Paragraph function</dt><dd>Function in English.</dd>
      <dt>Logical role</dt><dd>Logical role in English.</dd>
      <dt>Critical commentary</dt><dd>Text-based assessment in English.</dd>
    </dl>
    <dl class="analysis-ko" lang="ko">
      <dt>문단의 기능</dt><dd>문단의 기능 설명.</dd>
      <dt>논증에서의 역할</dt><dd>논리적 역할 설명.</dd>
      <dt>비판적 검토</dt><dd>본문에 근거한 평가.</dd>
    </dl>
  </aside>
</div>
```

Use the `thesis`, `concept`, `evidence`, `concession`, and `method` classes on marks and cards. Omit the category class for a neutral card. Keep marked text inside the exact English source. Escape HTML metacharacters in source and editorial text so the browser renders the original characters. Use semantic markup for lists, citations, equations, figures, captions, tables, and footnotes. A standalone source object may span the reading area where its width requires it. Keep its numbering and placement, translate substantive labels and captions as appropriate, and annotate caption paragraphs when they contribute to the argument. Use `.wide-content` for wide tables or equations that need a local horizontal scrollbar.

## Argument overview

At `@@ARGUMENT_OVERVIEW@@`, give the reasoning path as an ordered list when the paper follows a sequence. Use a nested list when it branches. Use headings for the reasoning path, one-sentence thesis, strongest argument, and weakest argument. Give each item English and Korean variants using `.analysis-en[lang="en"]` and `.analysis-ko[lang="ko"]` in that order. Link each analytical claim to the relevant paragraph, table, figure, or equation where feasible. Use `.analysis-en` and `.analysis-ko` for analysis visible in bilingual mode. Use `.label-en` and `.label-ko` for interface labels that change language in Korean mode.

## Check in the browser

- Open the final file locally. Confirm that the initial view shows English analysis and hides Korean translations. Toggle the translations on and off and confirm that the annotation language stays English.
- Switch to bilingual mode. For each paragraph, confirm that the English original precedes its Korean translation and the annotation shows English followed by Korean. Check the same order in the overview.
- Switch to Korean mode. Confirm that both source languages remain visible and the annotations, navigation, and overview use Korean.
- Follow each major-section link and confirm that the sticky bar leaves the heading visible and indicates the current section. Check desktop side-by-side alignment, mobile stacking, and access to every navigation link on a narrow screen.
- Check that the file renders with networking disabled. Confirm that figures, tables, equations, and legend colors still render correctly and all internal IDs resolve.
