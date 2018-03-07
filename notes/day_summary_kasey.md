The golang API group tried to find a way to port the most important concepts of STAC into WFS. Our proposal is to treat STAC as a WFS "Profile", which would include:


- Collections with homogenous schemas
- Schemas extension, types represented as json-schema
- Response model representing core fields (id, geometry, start, end)
- An opinionated extention for filtering (TBD), which would extend the base WFS filtering slightly beyond bbox and exact matches
- traversal API (w/ html rendered based on accept encoding) for scraping purposes

In order to prove this concept, we are planning to extend the go-wfs server with a provider that can serve a flat file catalog from a local filesystem.
