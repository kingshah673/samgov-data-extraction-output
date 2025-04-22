
# SAM.gov Scraper

A Python-based web scraper that extracts procurement opportunities from [SAM.gov](https://sam.gov/) (System for Award Management) using hidden APIs.

**Developer**: Syed Hasnain Abbas  
**Email**: hasnain.abbas32@outlook.com | kingshha673@gmail.com  
**GitHub**: [kingshah673](https://github.com/kingshah673/)

---

## Features
- Extracts opportunity data from SAM.gov's hidden APIs
- Parses JSON responses into structured data
- Handles pagination and multiple API endpoints
- Outputs clean, formatted results with:
  - Basic opportunity info (title, dates, IDs)
  - Classification details (NAICS, PSC, set-asides)
  - Contact information
  - Descriptions and attachments
  - Organizational hierarchy

## Example Output
```{
  "set_aside": "Total Small Business Set-Aside (FAR 19.5)",
  "naics_code": "335220 - Major Household Appliance Manufacturing",
  "product_service_code": "7290 - MISCELLANEOUS HOUSEHOLD AND COMMERCIAL FURNISHINGS AND APPLIANCES"
}
```

# Classification
```
{
"set_aside": "Total Small Business Set-Aside (FAR 19.5)",
"naics_code": "335220 - Major Household Appliance Manufacturing",
"product_service_code": "7290 - MISCELLANEOUS HOUSEHOLD AND COMMERCIAL FURNISHINGS AND APPLIANCES"
}

```

## API URL: `https://sam.gov/api/prod/watchlistservice/v1/api/toggle/enablecontractdata?random=17453590439571
## API URL: `https://sam.gov/api/prod/alerts

```

[
{
"alertID": 585,
"priority": 3,
"createdDate": "2025-03-08T05:54:54",
"lastModifiedDate": "2025-03-10T09:04:50",
"content": {
"title": "Subaward Reporting is live on SAM.gov",
"description": "<p>As of March 8th 2025, FSRS.gov has retired, and users should complete all subaward reporting in SAM.gov now.</p><ul><li><p>Find about the transition at <a href='\"http://sam.gov/FSRS\"'><u>SAM.gov/FSRS</u></a>. </p></li><li><p>Find more about managing and searching subawards at <a href='\"https://sam.gov/subaward-reports-help\"'>Subaward Reports</a>.</p></li><li><p>Find more about managing and searching subcontracts at <a href='\"https://sam.gov/subcontract-reports-help\"'>Subcontract Reports.</a></p></li></ul>",
"severity": "Informational",
"published": "2025-03-08"
}
},
{
"alertID": 580,
"priority": 3,
"createdDate": "2025-02-11T12:49:37",
"lastModifiedDate": "2025-04-22T10:52:23",
"content": {
"title": "Scheduled SAM Maintenance",
"description": "<p>SAM.gov will undergo planned maintenance on <strong>Saturday, May 10, 2025</strong> from 8:00 AM to 1:00 PM EST. Users in SAM.gov will be unable to complete Entity Registrations and Exclusions during this window.  Thank you for your understanding.</p>",
"severity": "Informational",
"published": "2025-04-22"
}
}
]

```

## API URL: `https://sam.gov/api/prod/opps/v2/dictionaries?random=1745359044516&amp;ids=fo_justification_authority,additional_reporting,ja_statutory_authority,justification_aquisition_authority

```

{
"_embedded": {
"dictionaries": [
{
"elements": [
{
"parentElementId": null,
"elementId": "brand",
"code": "brand",
"value": "FAR 6.302-1(c) - Brand name",
"description": null,
"active": true,
"sortIndex": 1,
"elements": null
},
{
"parentElementId": null,
"elementId": "far1",
"code": "far1",
"value": "FAR 6.302-1 - Only one responsible source (except brand name)",
"description": null,
"active": true,
"sortIndex": 2,
"elements": null
},
{
"parentElementId": null,
"elementId": "far2",
"code": "far2",
"value": "FAR 6.302-2 - Unusual and compelling urgency",
"description": null,
"active": true,
"sortIndex": 3,
"elements": null
},
{
"parentElementId": null,
"elementId": "far3",
"code": "far3",
"value": "FAR 6.302-3 - Industrial mobilization; engineering, developmental or research capability; or expert services",
"description": null,
"active": true,
"sortIndex": 4,
"elements": null
},
{
"parentElementId": null,
"elementId": "far4",
"code": "far4",
"value": "FAR 6.302-4 - International agreement",
"description": null,
"active": true,
"sortIndex": 5,
"elements": null
},
{
"parentElementId": null,
"elementId": "far5",
"code": "far5",
"value": "FAR 6.302-5 - Authorized or required by statute",
"description": null,
"active": true,
"sortIndex": 6,
"elements": null
},
{
"parentElementId": null,
"elementId": "far6",
"code": "far6",
"value": "FAR 6.302-6  - National security",
"description": null,
"active": true,
"sortIndex": 7,
"elements": null
},
{
"parentElementId": null,
"elementId": "far7",
"code": "far7",
"value": "FAR 6.302-7 - Public interest",
"description": null,
"active": true,
"sortIndex": 8,
"elements": null
}
],
"id": "ja_statutory_authority"
},
{
"elements": [
{
"parentElementId": null,
"elementId": "none",
"code": "none",
"value": "None",
"description": "",
"active": true,
"sortIndex": 1,
"elements": null
},
{
"parentElementId": null,
"elementId": "recovery_act",
"code": "recovery_act",
"value": "Recovery and Reinvestment Act",
"description": "",
"active": true,
"sortIndex": 2,
"elements": null
}
],
"id": "additional_reporting"
},
{
"elements": [
{
"parentElementId": null,
"elementId": "1",
"code": "1",
"value": "Urgency",
"description": null,
"active": true,
"sortIndex": 1,
"elements": null
},
{
"parentElementId": null,
"elementId": "2",
"code": "2",
"value": "Only One Source (except brand name)",
"description": null,
"active": true,
"sortIndex": 2,
"elements": null
},
{
"parentElementId": null,
"elementId": "3",
"code": "3",
"value": "Follow-on Delivery Order Following Competitive Initial Order",
"description": null,
"active": true,
"sortIndex": 3,
"elements": null
},
{
"parentElementId": null,
"elementId": "4",
"code": "4",
"value": "Minimum Guarantee",
"description": null,
"active": true,
"sortIndex": 4,
"elements": null
},
{
"parentElementId": null,
"elementId": "5",
"code": "5",
"value": "Other Statutory Authority (e.g. 8a, etc.)",
"description": null,
"active": true,
"sortIndex": 5,
"elements": null
}
],
"id": "fo_justification_authority"
},
{
"elements": [
{
"parentElementId": null,
"elementId": "far13",
"code": "far13",
"value": "FAR 13.5 - Simplified Procedures for One Source",
"description": "",
"active": true,
"sortIndex": 1,
"elements": null
}
],
"id": "justification_aquisition_authority"
}
]
},
"_links": {
"self": {
"href": "https://86samdotgovopportunitiesmodern.prod.apps-internal.prod-iae.bsp.gsa.gov/opps/v2/dictionaries?ids=fo_justification_authority%2Cadditional_reporting%2Cja_statutory_authority%2Cjustification_aquisition_authority\&ids=fo_justification_authority%2Cadditional_reporting%2Cja_statutory_authority%2Cjustification_aquisition_authority\&random=1745359044516"
}
}
}

```

## API URL: `https://sam.gov/api/prod/opps/v2/opportunities/34752cf5d3cc47a09494515e014bb8da?random=1745359044519

```

{
"data2": {
"type": "k",
"award": {},
"naics": [
{
"code": [
"335220"
],
"type": "primary"
}
],
"title": "FY25 Dorm Furniture and Appliances",
"archive": {
"date": "2025-05-17",
"type": "auto15"
},
"version": "2",
"permissions": {
"IVL": {
"read": true,
"create": true,
"delete": true,
"update": true
}
},
"solicitation": {
"setAside": "SBA",
"deadlines": {
"response": "2025-05-02T10:00:00-07:00",
"responseTz": "America/Los_Angeles"
}
},
"organizationId": "100242405",
"pointOfContact": [
{
"fax": "",
"type": "primary",
"email": "nakia.hightower_clements@us.af.mil",
"phone": "5092474872",
"title": null,
"fullName": "Nakía Hightower"
},
{
"fax": "",
"type": "secondary",
"email": "benjamin.hampton.1@us.af.mil",
"phone": "5092472234",
"title": null,
"fullName": "Benjamin Hampton"
}
],
"classificationCode": "7290",
"placeOfPerformance": {
"zip": "99011",
"city": {
"code": "22955",
"name": "Fairchild Air Force Base"
},
"state": {
"code": "WA",
"name": "Washington"
},
"country": {
"code": "USA",
"name": "UNITED STATES"
}
},
"solicitationNumber": "FA462025QA937",
"additionalReporting": [
"none"
]
},
"additionalInfo": {
"sections": [
{
"id": "header",
"status": "updated"
},
{
"id": "general",
"status": "updated"
},
{
"id": "classification",
"status": "updated"
},
{
"id": "description",
"status": "updated"
},
{
"id": "attachments-links",
"status": "updated"
},
{
"id": "contact",
"status": "updated"
}
]
},
"parent": {
"opportunityId": "e73215267d2f493f8c6c8e5ed8ca15ad"
},
"related": {},
"status": {
"code": "published",
"value": "Published"
},
"archived": false,
"cancelled": false,
"latest": true,
"deleted": false,
"postedDate": "2025-04-22T21:40:13.286+00:00",
"modifiedDate": "2025-04-22T21:40:13.290+00:00",
"createdDate": "2025-04-22T21:30:28.551+00:00",
"modifiedBy": "nakia.hightower_clements@us.af.mil",
"createdBy": "nakia.hightower_clements@us.af.mil",
"description": [
{
"opportunityId": "34752cf5d3cc47a09494515e014bb8da",
"descriptionId": "81641911c86e4e83a5e4acae4d4282a8",
"modifiedOn": "2025-04-22T21:40:13.291+00:00",
"body": "<p>The contractor shall provide Dorm Furniture and Appliances, in accordance with the attached Statement of Work and deliver to Fairchild AFB, WA.<br>\n<br>\nProposal due date was extended until 2 May 2025 by 10:00 A.M. PST in Amedment 001. Please see the attached 25QA937 - Amend001 -  Combo.</p>\n"
}
],
"totalCount": 1,
"_links": {
"self": {
"href": "/opps/v2/opportunities/34752cf5d3cc47a09494515e014bb8da"
},
"opportunity:publish:latest": {
"href": "/opps/v2/opportunities/34752cf5d3cc47a09494515e014bb8da"
},
"opportunity:previous": {
"href": "/opps/v2/opportunities/7a5f8464a498455f99d5e01bc5c166f7"
}
},
"opportunityId": "34752cf5d3cc47a09494515e014bb8da",
"id": "34752cf5d3cc47a09494515e014bb8da"
}

```

## API URL: `https://sam.gov/api/prod/opps/v2/dictionaries?random=1745359044523&amp;ids=farcases_type

```

{
"_embedded": {
"dictionaries": [
{
"elements": [
{
"parentElementId": null,
"elementId": "FAR 7.107-2",
"code": "FAR 7.107-2",
"value": "Intent to consolidate requirements",
"description": "Determination that consolidation is necessary and justified with the publication of the solicitation in Description.",
"active": true,
"sortIndex": 1,
"elements": null
},
{
"parentElementId": null,
"elementId": "FAR 7.107-3",
"code": "FAR 7.107-3",
"value": "Intent to bundle requirements",
"description": "Determination that bundling is necessary and justified with the publication of the solicitation in Description.",
"active": true,
"sortIndex": 2,
"elements": null
},
{
"parentElementId": null,
"elementId": "FAR 7.107-4",
"code": "FAR 7.107-4",
"value": "Intent to substantially bundle requirements",
"description": "Include the rationale for substantial bundling as part of the determination for bundling with the publication of the solicitation.",
"active": true,
"sortIndex": 3,
"elements": null
}
],
"id": "farcases_type"
}
]
},
"_links": {
"self": {
"href": "https://86samdotgovopportunitiesmodern.prod.apps-internal.prod-iae.bsp.gsa.gov/opps/v2/dictionaries?ids=farcases_type\&ids=farcases_type\&random=1745359044523"
}
}
}

```

## API URL: `https://sam.gov/api/prod/locationservices/v1/api/psc?random=1745359044851&amp;q=7290&amp;active=ALL&amp;advanceSearch=N&amp;searchby=psc&amp;asOfDate=2025-05-22

```

{
"_embedded": {
"productServiceCodeList": [
{
"pscId": 6966,
"pscCode": "7290",
"pscName": "MISCELLANEOUS HOUSEHOLD AND COMMERCIAL FURNISHINGS AND APPLIANCES",
"pscFullName": "Miscellaneous Household and Commercial Furnishings and Appliances",
"pscInclude": "Fireplace Sets; Vases and Urns; Household Sewing Machines.",
"activeInd": "Y",
"parentPscCode": "72 - HOUSEHOLD/COMMERC FURNISH/APPLIANCE",
"activeStartDate": "2011-10-01",
"updatedDate": "2024-04-30",
"_links": {
"self": {
"href": "https://65locationservicesprod.apps.prod-iae.bsp.gsa.gov/locationservices/psc?searchby=psc\&q=7290"
}
}
}
]
},
"_links": {
"self": {
"href": "https://65locationservicesprod.apps.prod-iae.bsp.gsa.gov/locationservices/psc"
}
}
}

```

## API URL: `https://sam.gov/api/prod/locationservices/v3/api/naics?random=1745359044853&amp;q=335220&amp;active=ALL&amp;asOfDate=2025-05-22&amp;size=6

```

{
"_embedded": {
"nAICSList": [
{
"naicsId": 9862,
"naicsCode": "335220",
"naicsTitle": "Major Household Appliance Manufacturing ",
"naicsSize": "6",
"parentNaicsCode": "33522",
"activeInd": "Y",
"sourceYear": "2022",
"_links": {
"self": {
"href": "https://65locationservicesprod.apps.prod-iae.bsp.gsa.gov/locationservices/v3/api/naics?sourceyear=2022\&code=335220"
}
}
}
]
},
"_links": {
"self": {
"href": "https://65locationservicesprod.apps.prod-iae.bsp.gsa.gov/locationservices/v3/api/naics{?sourceyear,code,asOfDate,q,size,active,setaside}",
"templated": true
}
}
}

```

## API URL: `https://sam.gov/api/prod/locationservices/v1/api/setAside?random=1745359044855&amp;q=SBA&amp;organizationIds=&amp;active=ALL&amp;activeStartDate=&amp;activeEndDate=

```

{
"_embedded": {
"setAsideList": [
{
"setAsideId": 12,
"setAsideCode": "SBA",
"setAsideName": "Total Small Business Set-Aside (FAR 19.5)",
"parentSetAsideCode": null,
"active": "Y",
"organizationIds": null,
"sortIndex": 25,
"legacyFBOCode": "7",
"activeStartDate": null,
"activeEndDate": null,
"_links": {
"self": {
"href": "https://65"
}
}
}
]
},
"_links": {
"self": {
"href": "https://65locationservicesprod.apps.prod-iae.bsp.gsa.gov/locationservices/setAside{?q,organizationIds,active,activeStartDate,activeEndDate}",
"templated": true
}
}
}

```

<div style="text-align: center">⁂</div>

[^1]: https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/63773998/7f679849-c04b-49b3-8771-8f707157d1cd/paste.txt```

