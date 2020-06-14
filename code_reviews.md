# What is this document about?

The tldr of this document is that I would like to create easy reviewable PRs and leave good reviews. However, it is also a way for me to re-iterate on my ideas and share things that I find working for me. Perhaps this document could help someone else who are striving for the same thing? 

When I'm an author of a PR I often find myself thinking "How can I make this as easily reviewable as possible?". On the other hand, when I'm reviewing I often think along the lines of "What is it again that I want to look for in a review? I remember the first three things but after that..".

Throughout this document I'll try to give my take on the two question above. Note that my reasoning is by no means the hole grail or a finished thought for that matter. This document reflects my current thinking as of writing this and you might have great ideas that I might be missing. If so, don't hesistate to submit either a PR for conversation or dm me directly.

## My assumptions for PRs

Before asking for a review or taking part of reviewing a PR I have a set of "assumptions" or perhaps ground rules.

1. Be humble(!). No matter how smart or brilliant your opinion is, if I feel offended or attacked I won't see things with an open mind, or atleast, I'll have a harder time doing so. Be a decent human being, show some respect it doesn't cost a thing :).

2. Opinions and thoughts around a PR is great, but don't expect the author of the PR to implement all your suggestions. Just like driving, there are quite a lot of ways to reach the end destination. Discuss trade-offs.

3. Assume good intent, this goes both ways.

4. The reviewer are the author are a team with the intention to build something great together. When suggesting changes refer to them in the terms of "we" and in the form of a question.

5. The reviewer is reponsible for rerviewing something "properly" before making an approval.

6. The author is reponsible for making sure the PR works as expected before and after deploy. This also includes follow up that might be necessary when things break etc.

## Am I done checking what I would like to check?

Now that we've covered my ground rules for a pull request lets dig into the checklist that you've been waiting for. The list below is not in a particular order and I'm not telling you that all of this should be done. It is a list with potential things that you could look at. I hope the list might help you with some new perspectives or at least be something you can look back at to feel more confident in smashing that approval button. It does for me at least...

1. **Do I understand the consequences of this PR good enough?** If not, are there any questions that I can ask the author to understand more? If you still don't understand enough? Great! There might be a chance to learn something by reviewing it together with someone that has a better understandinig.

2. **Do I understand why this change is suggested?** If not, ask the author to clarify.

3. **Are there sufficient tests for the change?**

4. **Is there a huge risk in rolling out the change?** Could we minimize impact? Feel free to ask the author on how they are thinking around this topics

5. **Is the solution building us into a corner?** A good feeling for when this is the case is when we can't extend on the solution. Perhaps we might have related required changes in the future but by making this change we no longer have the option to extend without modifying existing behaviour. 

Your gut feeling is "this is hacky", trust your gut. 

6. Are there any duplication?

7. Do we have metrics to monitor the change?

8. Do we have approperiate logging in place?

9. Are we duplicating something that could be refactored out and reused?

10. How have we tested the solution to make sure it works? You might be able to test it locally yourself if there is room.

11. Does the dependencies we are adding make sense? Could we remove any? Perhaps it makes sense to add an interface between?

12. Could there be any concurrency issues?

13. Is the code readable? Is the intention clear? If there are a bunch of comments there is probably an opportunity to refactor.

14. Does the code do what the author states?

15. Are there any edge cases we might have forgotten to consider?

16. Does the PR contain any scope creep that is bloating the PR?

17. Could there be any locking issues?

18. Are we imposing a security risk?

19. Are the changes made in a suitable place? In the right abstraction? Does it feel showed in?

20. Is the PR over engineering for something that might not be need?

21. Is the PR locking us into a decision that could be postponed?

22. Are the change backward/forward compatible.
