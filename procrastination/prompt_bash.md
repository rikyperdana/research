# Execute by: cat fileName.md | bash
# Separate each commands by line
# Remember: comment out completed tasks

# ollama run gemma3n:L "Based on the detailed plan from table of contents, conceptual understanding of the phenomenon represented in the variables, and supporting references I provided below, please write a detailed introduction part for this paper. All contents in this part should be only in paragraphs and few tables (if necessary), citations from the refered papers is recommended. The flow of the introduction part should be from the most generic perspective and narrow down to the specific concept and ended with the hypothetical research questions." < toc.md < references.md < variables.md >> introduction.md

# ollama run gemma3n:L "Based on the detailed plan from table of contents, conceptual understanding of the phenomenon represented in the variables, and supporting references I provided below, please write a detailed literature review part for this paper. All contents in this part should be only in paragraphs and few tables (if necessary), citations from the refered papers is recommended. What I expect from this part first is to identify different perspectives and findings among past researches and finding the right gap which supposed to be discovered, prove, or disproven by this research, which shall be the novelty of this research. Write as comprehensive as you can." < toc.md < references.md < variables.md >> literature_review.md

# ollama run gemma3n:L "Based on the detailed plan from table of contents, conceptual understanding of the phenomenon represented in the variables, please write a detailed methodology part for this paper. Use any relevant formulas if necessary. Write as comprehensive as you can." < toc.md < introduction.md < literature_review.md < variables.md >> methodology.md

# ollama run gemma3n:L "Based on this draft, please build a comprehensive questionaire involving relevant variables to be made into a google form format. First, write a preface to introduce the respondents what this research is about, then collect personal and demography data. For the questionarie, please involve all relevant variables and build for each of them statement items to be responded in Likert scale 1 to 5, signifying strong disagreement to strong agreement" < toc.md < introduction.md < literature_review.md < methodology.md >> questionaire.md

ollama run gemma3n:L "Tolong terjemahkan kuesioner ini ke dalam bahasa indonesia karena akan segera dibagikan" < questionaire.md >> kuesioner.md
