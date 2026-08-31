# One Shot Prompt

Provides exactly one example with request and the model learns the pattern, format, and style with that one example. It is useful for establishing format.

Choose the example carefully because it will set the pattern.

Include all elements you want on the output.

"Show don't tell": it's more effective to provide a single example of the desired output format rather than writing lengthy paragraphs of instructions about what to do and not do.

## Examples
```md
Write an engaging introduction for a blog post about remote work productivity.

Example:
Topic: Benefits of morning exercise
Introduction: "Picture this: It's 6 AM, your alarm goes off, and instead of hitting snooze, you lace up your sneakers. Sound impossible? Here's the thing—those who exercise before breakfast report 23% higher energy levels throughout their workday. But the real secret isn't just the exercise itself; it's what happens to your brain chemistry in those precious morning hours."

Now write an introduction for: Remote work productivity tips
```

```md
You are helping develop a prompt library application. Here's an example of how to analyze and implement a new feature:

**EXAMPLE:** Feature Request: "Add a favorites/bookmarking system"

Implementation Plan:

1. **User Story**: As a user, I want to mark prompts as favorites so I can quickly access my most-used prompts without scrolling through the entire library.
2. **Technical Requirements**:
    - Add a heart/bookmark icon to each prompt card
    - Store favorite status in localStorage or database
    - Create a filter to show only favorited prompts
    - Visual indicator when a prompt is favorited (filled vs outlined icon)
3. **Code Structure**:

javascript
// Data model update
prompt = {
  id: 'prompt-123',
  title: 'Marketing Email Generator',
  content: '...',
  isFavorite: false,  // New field
  createdAt: '2024-01-15',
  rating: 4.5
}

// Toggle favorite function
function toggleFavorite(promptId) {
  const prompt = prompts.find(p => p.id === promptId);
  prompt.isFavorite = !prompt.isFavorite;
  saveToStorage(prompts);
  updateUI();
}

4. **UI/UX Considerations**:
    - Place favorite icon in consistent location (top-right of card)
    - Use intuitive icons (heart or star)
    - Provide visual feedback on click (animation/color change)
    - Add "Favorites" filter tab in navigation

---

**YOUR TASK:** Analyze the following feature request using the EXACT same format as the example above (User Story, Technical Requirements with bullet points, Code Structure with JavaScript examples, and UI/UX Considerations).

Feature Request: "Add a 5-star rating component to rate prompt effectiveness"
```
