# Reference
<details><summary><code>client.<a href="src/tropicalia/client.py">search</a>(...) -&gt; AsyncHttpResponse[SearchResponse]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Perform a semantic search across project documents
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.search(
    project_id="proj_9f8b7c6d",
    query="Best practices for sustainable tropical agriculture",
    retrieval_strategy="hybrid",
    expand_query=False,
    rerank=True,
    generate_answer=True,
    include_sources=True,
    limit=50,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` — Project ID to search within
    
</dd>
</dl>

<dl>
<dd>

**query:** `str` — Search query text (max 2048 tokens)
    
</dd>
</dl>

<dl>
<dd>

**retrieval_strategy:** `typing.Optional[RetrievalStrategy]` 
    
</dd>
</dl>

<dl>
<dd>

**expand_query:** `typing.Optional[bool]` — Generate query variations to improve recall
    
</dd>
</dl>

<dl>
<dd>

**rerank:** `typing.Optional[bool]` — Rerank results using Cohere for improved relevance
    
</dd>
</dl>

<dl>
<dd>

**generate_answer:** `typing.Optional[bool]` — Generate a natural-language answer
    
</dd>
</dl>

<dl>
<dd>

**include_sources:** `typing.Optional[bool]` — Include source documents in response. Set false to reduce payload when only the answer is needed.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum results to return
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Projects
<details><summary><code>client.projects.<a href="src/tropicalia/projects/client.py">list_projects</a>(...) -&gt; AsyncHttpResponse[typing.List[Project]]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all projects for the authenticated user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.projects.list_projects()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**skip:** `typing.Optional[int]` — Number of projects to skip
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of projects to return
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.projects.<a href="src/tropicalia/projects/client.py">create_project</a>(...) -&gt; AsyncHttpResponse[Project]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new project
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.projects.create_project(
    name="Tropical Rainforest Conservation",
    description="A project focused on preserving tropical rainforest biodiversity.",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.projects.<a href="src/tropicalia/projects/client.py">get_project</a>(...) -&gt; AsyncHttpResponse[Project]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a specific project by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.projects.get_project(
    project_id="proj_9f8b7c6d",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.projects.<a href="src/tropicalia/projects/client.py">update_project</a>(...) -&gt; AsyncHttpResponse[Project]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a project by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.projects.update_project(
    project_id="proj_9f8b7c6d",
    name="Tropical Rainforest Conservation",
    description="A project focused on preserving the biodiversity of tropical rainforests.",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.projects.<a href="src/tropicalia/projects/client.py">delete_project</a>(...) -&gt; AsyncHttpResponse[ProjectDeleteResponse]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a project and all its documents
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.projects.delete_project(
    project_id="proj_9f8d7c2a",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Upload
<details><summary><code>client.upload.<a href="src/tropicalia/upload/client.py">file</a>(...) -&gt; AsyncHttpResponse[UploadResponse]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Upload a file for processing and indexing. Max 100MB.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.upload.file(
    project_id="projectId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` — Project ID to upload the file to
    
</dd>
</dl>

<dl>
<dd>

**file:** `from __future__ import annotations

core.File` — See core.File for more documentation
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.upload.<a href="src/tropicalia/upload/client.py">list_documents</a>(...) -&gt; AsyncHttpResponse[typing.List[Document]]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all documents in a project
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.upload.list_documents(
    project_id="proj_9f8b7c6d5e4a3b2c1d0e",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**skip:** `typing.Optional[int]` — Number of documents to skip
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of documents to return
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.upload.<a href="src/tropicalia/upload/client.py">delete_document</a>(...) -&gt; AsyncHttpResponse[DocumentDeleteResponse]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a document from the project
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from tropicalia import tropicalia

client = tropicalia(
    token="YOUR_TOKEN",
)
client.upload.delete_document(
    project_id="proj_9f8b7c6d5e4a3b2c1d0e",
    document_id="3fa85f64-5717-4562-b3fc-2c963f66afa6",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**project_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**document_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

