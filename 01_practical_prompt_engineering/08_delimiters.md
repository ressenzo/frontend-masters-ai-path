# Delimiters

Characters (triple quotes, dashs, XML tags, markdown) that create boundaries in the prompts.

It is important to use semantic naming to make prompts easier to understando for both developers and LLM. Instead of using generic names like 'X', use descriptive names like 'user_schema', 'requirements', 'constraints', or 'examples'.

Delimiters support nesting and attributes for complex data organization. For example, it is possible to have a parent tag like <research_area> that contains nested tags like <topic> and <questions>. This creates clear hierarchies, such as distinguishing between example one, two, and three, making it obvious where each section starts and ends.

## Examples

```md
I need to research how existing tools handle prompt management and version control to inform architecture decisions for a prompt library I'm building and hoping to move to production. Please research and analyze different approaches using this structure:

<research_area>
<topic>Prompt Management Solutions</topic>
<questions>
- What tools currently exist for prompt library management?
</questions>
</research_area>

<research_area>
<topic>Collaboration Features</topic>
<questions>
- How do teams share Postman collections or Insomnia workspaces?
- What permission models exist in developer tools?
</questions>
</research_area>

<research_area>
<topic>Technical Implementation Details</topic>
<questions>
- What databases do similar tools use (research from their engineering blogs)?
- How do they handle search at scale?
- What's their approach to data export/import?
- How do they prevent abuse and implement rate limiting?
</questions>
</research_area>

For each research area:
1. Find concrete examples from real products
2. Identify patterns across successful tools
3. Highlight common failures or user complaints
4. Estimate implementation complexity

Then synthesize this into:
- A competitive analysis matrix
- Recommended features for our MVP vs future releases
- Technical decisions informed by market research
```
