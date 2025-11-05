# Africa Area Data

**Africa Area Data** is an **open-source project** that centralizes, structures, and makes accessible **all administrative geographic divisions of Africa**, from countries to regions, departments, communes, neighborhoods, and villages. All data uses a **single, standardized JSON format** for consistency and ease of use.

---

## Goal

Administrative geographic data in Africa is often **hard to find**, **incomplete**, or **scattered across multiple sources**. This project aims to:

* **Collect** reliable geographic data for every African country;
* **Standardize** all divisions into a **single JSON structure**, making it easy to use for developers, researchers, and institutions;
* **Share openly** to promote transparency, research, and innovation with open data in Africa.

---

## JSON Structure

Every geographic entity uses the same JSON structure. All fields below are optional except `name`, `type`, `parent`, and `code`:

| Field                       | Description                                                              | Example                                                            |
| --------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `name`                      | Official name of the zone                                                | `"Dakar"`                                                          |
| `type`                      | Type of zone (country, region, department, commune, neighborhood…)       | `"region"`                                                         |
| `parent`                    | Code of the parent division (null if top-level)                          | `"SN"`                                                             |
| `code`                      | Unique identifier for the division                                       | `"SN-DAK"`                                                         |
| `alt_names`                 | Alternative or historical names (useful for search or matching)          | `["Dakar Capital Region", "Région de Dakar"]`                      |
| `iso_code`                  | Official ISO code for countries or subdivisions, if available            | `"SN-DAK"`                                                         |
| `population`                | Number of inhabitants (census or estimated)                              | `1050000`                                                          |
| `area_km2`                  | Area in square kilometers                                                | `547`                                                              |
| `coordinates`               | Approximate geographical coordinates (latitude/longitude)                | `{"lat": 14.6928, "lng": -17.4467}`                                |
| `bounding_box`              | Geographic bounding box (useful for mapping/GIS)                         | `{"north": 14.83, "south": 14.66, "east": -17.35, "west": -17.55}` |
| `timezone`                  | Time zone                                                                | `"GMT+0"`                                                          |
| `status`                    | Administrative status (e.g., recognized, proposed, historical)           | `"recognized"`                                                     |
| `created_at` / `updated_at` | Creation date / last update of the data                                  | `"2025-01-01" / "2025-10-01"`                                      |
| `links` / `source`          | URL or reference of official source (INS, OCHA, UN, etc.)                | `["https://www.stat-sn.gov.sn/"]`                                  |
| `notes`                     | Additional information or context (e.g., disputed areas, recent changes) | `"Capital region of Senegal"`                                      |
| `neighbors`                 | Codes of neighboring zones (useful for geographic analysis)              | `["SN-THI", "SN-RUF"]`                                             |

### Example

```json
{
  "name": "Dakar",
  "alt_names": ["Dakar Capital Region", "Région de Dakar"],
  "type": "region",
  "parent": "SN",
  "code": "SN-DAK",
  "iso_code": "SN-DAK",
  "population": 1050000,
  "area_km2": 547,
  "coordinates": {"lat": 14.6928, "lng": -17.4467},
  "bounding_box": {"north": 14.83, "south": 14.66, "east": -17.35, "west": -17.55},
  "timezone": "GMT+0",
  "status": "recognized",
  "created_at": "2025-01-01",
  "updated_at": "2025-10-01",
  "links": ["https://www.stat-sn.gov.sn/"],
  "notes": "Capital region of Senegal",
  "neighbors": ["SN-THI", "SN-RUF"]
}
```

---

## Possible Uses

* Mapping and GIS (Geographic Information Systems)
* Development of government or civic applications
* Data science and territorial analysis projects
* Visualization and geolocation of public infrastructure
* Demographic, electoral, or economic studies

---

## 🤝 Contribution

We welcome contributions from everyone! You can:

* Add or correct data for any country;
* Improve JSON structures or consistency;
* Ensure **accuracy, verifiability, and source citation** for all data;
* Help with documentation and validation of sources.

**Guidelines for data contributions:**

* Data must be **accurate and sourced** (INS, OCHA, UN, government sources, etc.).
* Follow the **standard JSON structure**.
* Document any modifications clearly.

---

## Code of Conduct (Summary)

We aim to create a **friendly, respectful, and collaborative environment**.

* **Be respectful**: treat others courteously.
* **Contribute responsibly**: ensure data is reliable and sourced.
* **Communicate constructively**: feedback should be helpful and polite.
* **Report issues**: notify maintainers of harassment, inappropriate behavior, or unreliable data.

Full Code of Conduct: see [Code of conduct](`./CODE_OF_CONDUCT.md`).

---

## License

Africa Area Data is licensed under the **Open Database License (ODbL) 1.0**.

* You are free to **share, adapt, and use commercially**.
* **Attribution is required**: include “Contains data from Africa Area Data, licensed under ODbL 1.0.”
* If redistributing the database or derivatives, you must **share under ODbL 1.0**.

Full license: see [`licence`](./LICENCE.md).

