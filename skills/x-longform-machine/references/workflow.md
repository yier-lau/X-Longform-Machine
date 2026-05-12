# Workflow

## 0. Human Review Gates

This machine is not fully automatic. It is a controlled production line.

At every branch that asks "whether" or "which direction", stop and ask the user to confirm before continuing.

Required review gates:

- topic angle confirmation
- goal clarity gate confirmation
- concept deconstruction gate confirmation
- article spine confirmation
- draft approval before style rewrite
- rewrite approval before publishing package
- publishing package approval before cover prompt
- privacy boundary confirmation before using sensitive material
- state save/restore/report confirmation

Use this review format:

```text
我建议下一步做：{step}
原因：{one sentence}
需要你确认后我再继续。
```

If the user explicitly says "直接做", "不用问我", or gives a specific next step, execute only that approved step. Return to review gates before the next strategic branch.

## 1. Intake

Identify what the user provided:

- raw idea
- article title
- rough notes
- existing draft
- request for rewrite
- request for publishing package
- request for cover prompt

If the request is actionable, proceed. Ask only when a missing decision would change the output materially.

If the next step involves choosing a direction, ask for confirmation first.

## 2. Material Selection

Gather only the minimum relevant corpus:

- style samples from sanitized diary blocks
- X posts/replies for platform voice
- worldview notes for AI/workflow/product/system claims
- personal story bank for lived scenes
- quote bank for reusable lines

Do not blindly summarize the whole archive.

## 3. Topic Judgment

Clarify the core claim in one sentence.

Stop after proposing the core claim and wait for user approval before drafting.

If the user's goal is vague, run a goal-clarity gate before writing:

- What concrete deliverable should this article create?
- Who should change their mind after reading it?
- What should the reader be able to repeat in one sentence?
- What future product, service, or personal asset can this article support?

Good X longform topics should have at least two of:

- counterintuitive judgment
- personal experience behind the claim
- clear audience pain
- relation to AI/workflow/personal system
- product or service extension potential
- quotable compressed line

If weak, strengthen the angle before drafting.

If strengthening changes the topic, ask the user to approve the new angle.

## 3.5 DBS Gates

Use these gates only when they help the article move forward:

- Goal clarity: use when the user says "做个人 IP", "有影响力", "更好", "表达自己", or similar vague targets.
- Concept deconstruction: use when the topic depends on fuzzy words such as Agent, Skill, Workflow, personal corpus, creativity, IP, influence, freedom, or system.
- Content diagnosis: use after there is a topic, outline, or draft.
- Hook optimization: use when the first screen is slow, abstract, or too explanatory.
- AI flavor check: use after a full draft exists.
- State save/report: use when an article direction, rejection, or final version should be remembered for later.

Do not run every gate every time. The machine should feel decisive, not bureaucratic.

Before any DBS gate, ask:

```text
这里我建议过一遍 {gate_name}，因为 {reason}。确认后我再做。
```

## 4. Article Spine

Build the article around this sequence:

1. Concrete personal scene or contradiction.
2. Old belief.
3. What broke that belief.
4. New judgment.
5. Why it matters now.
6. Personal proof or lived material.
7. Systemic explanation.
8. Practical implication.
9. Strong ending line.

Do not start with abstract definitions unless the topic requires concept explanation.

After building the spine, stop and ask the user to approve it before writing the full draft.

## 5. Draft

Write in longform X rhythm:

- short paragraphs
- one idea per paragraph
- first-person where useful
- enough repetition for rhythm, not redundancy
- no markdown headers in the publishable body unless the user asks

Default target length: 1,500 to 3,000 Chinese characters unless the user specifies otherwise.

After the draft, stop. Do not automatically style-rewrite, diagnose, package, or generate cover prompts unless the user approves the next step.

## 6. Style Rewrite

Rewrite once for the user's voice:

- make the opening more direct
- add lived texture
- remove generic advice
- add rough edges where natural
- keep private material abstract
- preserve useful tension and contradiction

Do not imitate sensitive diary content directly. Borrow rhythm, not secrets.

Before style rewrite, state which style sources will be referenced and ask for approval.

## 7. Clean AI Flavor

Remove:

- symmetrical list padding
- "in this era" filler
- generic "we need to"
- over-explained transitions
- empty conclusion paragraphs
- slogans not paid for by personal material

Keep:

- specific scenes
- decisive claims
- uncomfortable but true sentences
- lines that can stand alone as short posts

## 7.5 Publish Emphasis

Before a publish-candidate or final publish version, apply restrained bold emphasis.

Bold only:

- the opening core claim
- the main turn in the middle
- reusable high-compression lines
- the final landing line
- lines the user explicitly says are important

Do not bold every paragraph ending. Bold is not decoration; it is a reading handle for X longform.

## 7.6 Altruism And Save Value Check

Before generating the publishing package, check whether the article has reader utility and save value.

Do not judge only by hook, title, sharpness, or likely views. Ask:

- What concrete problem does this help the reader understand or solve?
- What reusable judgment, framework, checklist, question set, or method can the reader take away?
- Which part would someone save and return to later?
- Is the article only satisfying to the author, or useful to the reader?
- If the emotional punch is removed, what practical value remains?

For post-publication iteration, treat saves/bookmarks and save rate as key signals of altruism and long-term utility. Views measure reach; saves measure whether the piece was worth keeping.

Before rewriting based on AI flavor, ask whether the user wants diagnosis only or direct rewrite.

## 8. Publishing Package

When requested, output:

- main post opening
- full longform body
- 5 to 10 short posts for later reuse
- 2 to 4 comment follow-ups
- 3 follow-up article topics
- brief publishing note

Short posts and comment follow-ups are reusable assets, not just publishing-package byproducts.

Whenever a publishing package contains short posts or comment follow-ups:

- if the user has a configured personal archive root, also write the short posts to `{PERSONAL_EXPRESSION_ROOT}/08_资产库/17_短帖库/{date}_{article_title}_短帖.md`
- if the user has a configured personal archive root, also write the comment follow-ups to `{PERSONAL_EXPRESSION_ROOT}/08_资产库/18_评论区补充库/{date}_{article_title}_评论区补充.md`
- update each sublibrary's `索引.md` with the new entry
- keep a link from the publishing package to both asset entries
- mark public level and source article in both asset files

If the user has no archive root configured, keep short posts and comment follow-ups inside the publishing package and tell the user how to create these two libraries.

Do not split into thread by default. Recommend thread only when the structure naturally requires multiple linked parts.

Generate a publishing package only after the user confirms the draft is close enough to publish.

## 8.5 State Notes

When a longform project reaches a stable conclusion, optionally create a short state note:

- article title
- selected angle
- rejected angles
- best lines
- final version path
- next articles

If `dbs-save` is available and the user asks to preserve diagnosis state, use it. Otherwise, write a lightweight note under the longform system outputs.

Never save, restore, or report state without explicit user request or confirmation.

## 9. Cover Prompt

When the user needs a cover, use `cover-prompt.md`:

- extract a 2 to 8 character core visual phrase
- design a conceptual poster
- keep text embedded into the composition
- output a direct image prompt

Before generating the final cover prompt, ask the user to confirm:

- main visual words
- whether Chinese text should be generated in-image or reserved for manual typesetting
- forbidden visual elements

## 10. File Naming

Use Chinese filenames when user-facing.

Recommended suffixes:

- `_v1_初稿`
- `_v2_风格重写`
- `_v3_日记语感版`
- `_v4_融合发布版`
- `_v5_发布精修版`
- `_发布包`
- `_封面提示词`
