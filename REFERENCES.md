<!-- title: The Scientist References -->

# References

The methodology, checklists, and rubrics implemented in this project's
agents and skills were informed by the sources listed below, in
alphabetical order. This file documents provenance for transparency;
the agent/skill instruction files themselves are written as original
synthesis and do not carry inline citations, by design, so that the
operational prompts stay readable and authoritative on their own.

- `github.com/Amirhorikini/academic-research-skills`. A separate, more
  elaborate project by the same author (multi-skill pipeline with a
  7-agent reviewer panel, JSON-schema-governed contracts, and
  cross-model verification). The Scientist's pipeline structure (staged
  agents, a shared rules file, a scoring rubric, a Devil's Advocate
  persona, re-review traceability) was adapted in simplified form from
  ideas in that project, not copied directly - the two projects differ
  substantially in scope and implementation. Later additions also
  adapted, in simplified form, from specific reference/template files in
  that repo's `academic-paper-reviewer` skill: the statistical-reporting
  checklist and GRIM/GRIMMER red flags (used in
  `statistical-reporting-standards`), the R→A→C revision-response
  template (used in `revision-response-composer`), the Accept/Minor/
  Major/Reject decision matrix and symmetric-evidence principle (used in
  `scientific-boss`), and the three-lenses review framework (internal
  validity/external validity/contribution) plus common reviewer traps
  (used in `scientific-review`'s Lente Crítica).
- Bitesize Bio. "How to Read a Scientific Paper: A Quick & Effective
  Method." https://bitesizebio.com/11060/how-to-read-a-scientific-paper/
- Bitesize Bio. "How to Write a Scientific Review (And The Upstream Work
  That Makes It Easier)."
  https://bitesizebio.com/88546/how-to-write-a-scientific-review/
- Bitesize Bio. "How to Write an Authoritative Scientific Discussion
  Section." https://bitesizebio.com/31855/write-discussion-paper/
- Bitesize Bio. "Publish the Unpublishable: How to Publish Negative
  Results." https://bitesizebio.com/47728/publish-negative-results/
- Booth, W.C., Colomb, G.G., Williams, J.M. (later editions with Bizup,
  J. and FitzGerald, W.T.). *The Craft of Research*. University of
  Chicago Press. Multiple editions, 1995-2024 (5th ed. 2024). The
  claim/reason/evidence/warrant/acknowledgment-response argument
  structure used in `publication-strategist` was drawn indirectly via a
  third-party interactive summary of the 5th edition:
  https://businesssciencedaily.com/the-craft-of-research-booth-et-al-5th-ed-2024/
- CAPES (Coordenação de Aperfeiçoamento de Pessoal de Nível Superior).
  Portaria nº 206, de 25 de setembro de 2018 (mandatory funding
  acknowledgment for CAPES-supported work). Summarized via
  https://ccomp.ime.uerj.br/capes-formaliza-obrigatoriedade-de-citacao-em-trabalhos/
- Carey, M.A., Steiner, K.L., Petri, W.A. Jr. "Ten simple rules for
  reading a scientific paper." *PLOS Computational Biology* 16(7):
  e1008032 (2020). https://pmc.ncbi.nlm.nih.gov/articles/PMC7392212/
- Creswell, J.W., Creswell, J.D. *Research Design: Qualitative,
  Quantitative, and Mixed Methods Approaches*. 5th ed. SAGE
  Publications (2018). Also published in later editions (most recent:
  6th ed., updated to APA 7th edition style). Accessed indirectly via a
  publicly posted chapter-summary study guide:
  https://writingcenter.westcliff.edu/wp-content/uploads/2022/06/Creswell-Creswell-2018.pdf
- Desaire, H., Chua, A.E., Isom, M., Jarosova, R., Hua, D.
  "Distinguishing academic science writing from humans or ChatGPT with
  over 99% accuracy using off-the-shelf machine learning tools." *Cell
  Reports Physical Science* 4(6): 101426 (2023).
  https://www.cell.com/cell-reports-physical-science/fulltext/S2666-3864(23)00200-X
- Editora Dialética. "Revisão de artigos científicos." Blog post.
  https://editoradialetica.com/blog/revisao-de-artigos-cientificos/
- Elsevier Researcher Academy. "Navigating Peer Review" module.
  https://researcheracademy.elsevier.com/navigating-peer-review
- EQUATOR Network. "Enhancing the QUAlity and Transparency Of health
  Research." https://www.equator-network.org/ (source for the CONSORT,
  STROBE, PRISMA, SPIRIT, PRISMA-P, STARD, TRIPOD, CARE, AGREE,
  SRQR/COREQ, ARRIVE, SQUIRE, and CHEERS reporting checklists)
- Gopen, G.D., Swan, J.A. "The Science of Scientific Writing." *American
  Scientist* 78(6): 550-558 (1990). The topic-position/stress-position/
  subject-verb-separation principles used in `narrative-architecture`
  come from this paper. https://www.gatsby.ucl.ac.uk/~pel/misc/gopen_swan.pdf
- Halliday, M.A.K., Hasan, R. *Cohesion in English*. English Language
  Series. London: Longman (1976). Source for the grammatical-vs-lexical
  cohesion distinction referenced in `narrative-architecture`'s
  "invisible transitions" guidance (lexical cohesion as an alternative
  to mechanical connectors like "furthermore"/"moreover").
- Hunting the Muse. "How to Tell if Writing is AI."
  https://huntingthemuse.net/library/how-to-tell-if-writing-is-ai
- International Committee of Medical Journal Editors (ICMJE).
  "Recommendations for the Conduct, Reporting, Editing, and Publication
  of Scholarly Work in Medical Journals." https://www.icmje.org/recommendations/
- Kobak, D., González-Márquez, R., Horvát, E.-Á., Lause, J. "Delving
  into LLM-assisted writing in biomedical publications through excess
  vocabulary." *Science Advances* 11(27) (2025).
  https://pmc.ncbi.nlm.nih.gov/articles/PMC12219543/
- Koike, R., Kaneko, M., Okazaki, N. "OUTFOX: LLM-Generated Essay
  Detection Through In-Context Learning with Adversarially Generated
  Examples." *Proceedings of the AAAI Conference on Artificial
  Intelligence* (2024). (Note: user-suggested citation said "Findings
  of ACL 2023" - corrected here to the verified venue/year, AAAI 2024.)
  Cited only as context for why AI-text detection is an inherent arms
  race (detectors vs. adversarial generation), reinforcing this
  project's existing disclaimer that its style checklists are not a
  reliable AI detector - not used as a technique for evading detection.
  https://ojs.aaai.org/index.php/AAAI/article/view/30120
- Liang, W. et al. "Mapping the Increasing Use of LLMs in Scientific
  Papers." arXiv:2404.01268 (2024). Preprint predecessor of the same
  study's peer-reviewed version below (same lead author, same core
  finding, updated numbers) - listed together, not as independent
  confirmation.
- Liang, W. et al. "Quantifying large language model usage in
  scientific papers." *Nature Human Behaviour* (2025).
  https://doi.org/10.1038/s41562-025-02273-8
- Mensh, B., Kording, K. "Ten simple rules for structuring papers."
  *PLOS Computational Biology* 13(9): e1005619 (2017). The
  Context-Content-Conclusion (C-C-C) framework, the Introduction
  gap-progression structure, and the Results "sequence of statements"
  structure used in `narrative-architecture` come from this paper.
  https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005619
- Noble, W.S. "A quick guide to organizing computational biology
  projects." *PLOS Computational Biology* 5(7): e1000424 (2009).
  https://pmc.ncbi.nlm.nih.gov/articles/PMC2709440/
- ResearchRabbit. "How to Write a Research Paper: Step-by-Step Guide."
  https://www.researchrabbit.ai/articles/how-to-write-a-research-paper
- SAGE Research Methods. Platform of guides on research design,
  hypothesis alignment, and methodology selection. https://methods.sagepub.com/
- Simera, I., Moher, D., Hoey, J., Schulz, K.F., Altman, D.G.
  "Transparent and accurate reporting increases reliability, utility,
  and impact of your research: reporting guidelines and the EQUATOR
  Network." *BMC Medicine* 8: 24 (2010).
  https://doi.org/10.1186/1741-7015-8-24
- Swales, J.M. *Genre Analysis: English in Academic and Research
  Settings*. Cambridge University Press (1990). Source of the CARS
  (Create a Research Space) model - Move 1 (Establishing a Territory),
  Move 2 (Establishing a Niche), Move 3 (Occupying the Niche) - used in
  `narrative-architecture`'s Introduction-structure guidance.
- Wiley Online Library. "Immunity, Inflammation and Disease - Author
  Guidelines."
  https://onlinelibrary.wiley.com/page/journal/20504527/homepage/forauthors.html
- Zou, Y., Kuek, F., Ng, K.H., Cheng, X. "Comparative analysis of text
  readability and writing styles in AI-generated vs. human-written
  academic abstracts." *PLOS One* 21(4): e0343163 (2026).
  https://pmc.ncbi.nlm.nih.gov/articles/PMC13061212/

## Unpublished sources

- User-compiled notes and comparison tables (English vs. Portuguese
  academic-AI vocabulary/connector patterns, structural-variability and
  triptych-pattern observations, stylometry research-field overview),
  contributed directly by the project author during development
  (2026-08-19). Not sourced from a single published work, so not listed
  alphabetically above with the citable references.

## Unverifiable sources (deliberately excluded)

Per this project's own citation-verification rule, two sources
suggested during development were **not** added above because their
exact bibliographic details could not be confirmed via search:

- "Sciamanna, C.N., et al. (2000). How to write a scientific paper.
  Journal of General Internal Medicine" - no matching article found
  under this exact title/author/journal/year combination.
- "Sullivan, G.M. (2012). What editors want in a manuscript submission.
  Journal of Graduate Medical Education" - Sullivan has written related
  JGME editorials on submission quality and desk-rejection (e.g., a
  2025 piece, "Advice for Authors Considering Submitting to the Journal
  of Graduate Medical Education"), but this exact 2012 title could not
  be confirmed.

If either of these is genuinely needed later, re-verify with the exact
DOI or a direct link before citing.

## Note on currency

Some of these sources (journal author guidelines, ICMJE
recommendations, EQUATOR checklist list) can change over time. If a
review decision depends on a detail that might be outdated, re-fetch
the source rather than trusting this file's summary indefinitely.
