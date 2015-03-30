This contains data for the vocabulary learning program.  The format is
simple, with a backslash ``\`` between the two terms, one term pair per
line::

  hyvä \ good

All text should be UTF-8 encoded.  Case is preserved when showing the
terms, but is ignored when matching terms.

If a hint or clarification is needed, then put that in parentheses.
The part in parentheses will NOT be considered when matching in
correctness.  Thus, there should be only one non-parenthesized part
for each term (for both languages), which is a reasonable translation.
The parenthesized parts are shown in the translation prompt, as well
as the actual translated value, to aid comprehension::

   toinen \ second (other)

Verbs are allowed to have a ``/`` between the root and the stem.  This
is not required, but a convention from one of the earlier lists::

  ol/la   \ to be

Lines beginning with ``#`` are treated as comments.  Also, blank lines
are ignored::

  # This file came from some blog post
  ol/la   \  to be

If a file has English first, then Finnish, place the special string
``###reversed`` within the first few lines::

  ###reversed.
  to be   \   ol/la

