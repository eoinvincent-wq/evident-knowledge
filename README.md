# Evident Knowledge Base

> Comprehensive knowledge base of Evident Inspection products and solutions for AI/LLM consumption

##  Overview

This repository contains a structured knowledge base covering:
- **Nondestructive Testing (NDT)** equipment and solutions
- **X-ray Fluorescence (XRF)** analyzers
- **Ultrasonic Testing** systems (PAUT, conventional)
- **Remote Visual Inspection (RVI)** equipment
- **Industrial inspection** solutions across multiple industries

##  For AI/LLM Use

This knowledge base is specifically formatted for consumption by Large Language Models (LLMs) and AI assistants.

### Available Formats

- **Markdown**: [`website_llm_sitemap.md`](./website_llm_sitemap.md) - Human and LLM readable
- **JSON**: [`website_llm_sitemap.json`](./website_llm_sitemap.json) - Structured data format
- **URL List**: [`website_llm_sitemap_urls.txt`](./website_llm_sitemap_urls.txt) - All page URLs

### Direct Access URLs

```
# Markdown format
https://raw.githubusercontent.com/eoinvincent-wq/evident-knowledge/main/website_llm_sitemap.md

# JSON format  
https://raw.githubusercontent.com/eoinvincent-wq/evident-knowledge/main/website_llm_sitemap.json

# URL list
https://raw.githubusercontent.com/eoinvincent-wq/evident-knowledge/main/website_llm_sitemap_urls.txt
```

##  Dataset Statistics

- **Total Pages**: 4,329
- **Total Words**: 860,254
- **Source**: https://ims.evidentscientific.com
- **Last Updated**: November 2024

##  Industries Covered

- Aerospace
- Oil & Gas
- Manufacturing
- Mining & Geology
- Energy & Power Generation
- Automotive
- Infrastructure
- Electronics

##  Technologies Documented

- **XRF Analysis** (64 pages)
- **Vanta Series** (33 pages)
- **Phased Array Ultrasound** (25+ pages)
- **OmniScan Systems** (25 pages)
- **Thickness Measurement** (16 pages)
- **Eddy Current Testing** (11 pages)
- **Remote Visual Inspection** (20 pages)

##  Use Cases

### For Developers
- Build RAG (Retrieval Augmented Generation) systems
- Create chatbots about inspection equipment
- Develop product recommendation engines
- Integrate with existing AI assistants

### For Researchers
- Study nondestructive testing methodologies
- Compare inspection technologies
- Analyze industry applications

### For LLM Training
- High-quality technical documentation
- Real-world industrial applications
- Product specifications and use cases

## 🚀 Quick Start Examples

### OpenAI Assistant API
```python
from openai import OpenAI
client = OpenAI()

file = client.files.create(
  file=open("website_llm_sitemap.json", "rb"),
  purpose='assistants'
)

assistant = client.beta.assistants.create(
  name="Evident Scientific Expert",
  tools=[{"type": "file_search"}],
  tool_resources={"file_search": {"vector_stores": [{"file_ids": [file.id]}]}}
)
```

### LangChain
```python
from langchain_community.document_loaders import JSONLoader

loader = JSONLoader(
    file_path='website_llm_sitemap.json',
    jq_schema='.pages[]',
    text_content=False
)
docs = loader.load()
```

### Custom GPT
1. Go to ChatGPT → My GPTs → Create
2. Upload `website_llm_sitemap.md` as knowledge
3. Set instructions to reference Evident Scientific products

## 📖 Data Structure

Each page entry includes:
- **Title** and **URL**
- **Keywords** (technology, industry, application)
- **Description** and meta information
- **Main content** preview
- **Word count** and content structure
- **Headings hierarchy**

## 🔗 Related Resources

- **Official Website**: [ims.evidentscientific.com](https://ims.evidentscientific.com)
- **Product Catalog**: Detailed product information
- **Application Notes**: Technical guides and use cases
- **Industry Solutions**: Sector-specific applications

##  License & Usage

This knowledge base is provided for informational purposes and AI/LLM integration.
For commercial use, please refer to the terms at [evidentscientific.com](https://ims.evidentscientific.com).

Original content © Evident Scientific
Knowledge base compilation and formatting for AI use.

##  Contributing

Found an issue or want to suggest improvements?
- Open an issue
- Submit a pull request
- Contact: eoin.vincent@evidentscientific.com

##  Updates

This knowledge base is periodically updated to reflect:
- New product releases
- Updated specifications
- New application notes
- Industry developments

**Last crawl date**: November 12, 2024

---

**Keywords**: NDT, nondestructive testing, XRF, ultrasonic testing, phased array, PAUT, inspection equipment, industrial inspection, quality control, materials testing, flaw detection, thickness measurement, corrosion inspection, XRF analyzer, remote visual inspection, RVI, video borescope, AI knowledge base, LLM training data, RAG system
