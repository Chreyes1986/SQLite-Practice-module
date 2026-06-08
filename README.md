About this project
A self-contained SQL practice environment that runs entirely in your browser — no server, no install, no signup. It serves two parallel practice purposes:

1 · Data analysis practice
Three role-specific schemas (Clinical Operations, Financial Analysis, Marketing Analytics), each with realistic generated data and 30 progressively harder problems. Beginner covers SELECT, WHERE, ORDER BY, LIMIT, DISTINCT. Intermediate adds JOINs, GROUP BY, aggregation, and HAVING. Advanced introduces window functions (RANK, LAG, NTILE), CTEs, self-joins, and date math. Hit Refresh data to regenerate the database with new random values — same questions, different answers.

2 · AI-assisted creation practice
Building real applications iteratively with AI is a skill in its own right — breaking down a project, validating output, and directing the AI through revisions. This tool was built that way, end-to-end with Claude (Anthropic's AI assistant): spec, scaffold, test, refine. The whole thing is a single HTML file, deliberately, so it can be read end-to-end like a tutorial in how to compose a working app from clear sub-goals.

How to use
Pick a role from the Analyst role dropdown at the top.
Read the schema (Schema tab) or use the sidebar reference next to the editor.
Pick a problem from the dropdown in the Query tab, or browse the Practice tab.
Write your query, click Run to see results, click Check Answer to grade against the solution.
Status icons: ✓ green = completed · ✓ yellow = attempted.
Progress
Status and your selected role persist in this browser via localStorage. You can clear it any time:

Reset all progress
Built by Christian Reyes with Claude (Anthropic). Engine: SQLite (WebAssembly) via sql.js. Editor: CodeMirror.
