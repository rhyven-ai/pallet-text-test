# Text Kit test pallet

Small Apache-2.0 Python functions for normalizing whitespace and creating ASCII URL slugs. No dependencies or Rhyven imports.

This repository is a public distribution test for an unreleased Rhyven pallet format. It is not listed in the production marketplace. The fixture index contains only this library.

```python
from textkit import prepare_document
print(prepare_document({"title": "  Customer   Release Notes! "}))
# {"title": "Customer Release Notes!", "slug": "customer-release-notes"}
```

`slug` retains only ASCII a–z and 0–9. It does not transliterate Unicode or guarantee uniqueness; non-ASCII-only input may produce an empty slug.

Exports: `normalize`, `slug`, `rename_title`, and `prepare_document`. Each accepts one dictionary and returns one dictionary. `pallet.json` supplies typed contracts and example tests.
