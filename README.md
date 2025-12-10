# Steam-Data-Collection
Data collection and preprocessing code for published research on Steam game IDs, time-centric marketing language, and user review analysis.

This repository contains the notebooks used to collect Steam game IDs ordered by relevance (https://store.steampowered.com/search?term=) and retrieve related store-page metadata and user reviews for research on time-centric language in Steam user reviews.

The data collection workflow is structured as a small pipeline:
- Collect Steam game IDs ordered by relevance using the Steam store listing page.
- Parse these IDs into two collection pathways:
  - Store page metadata collection.
    <img width="759" height="69" alt="image" src="https://github.com/user-attachments/assets/0b89ed67-8ead-4d17-af6a-57729c977524" />

  - User review collection.
    <img width="1317" height="71" alt="image" src="https://github.com/user-attachments/assets/ed1f6357-7111-48b6-b71a-c16cf46ab0e4" />

The notebooks in this repository are adapted and edited versions of existing open-source tools, with modifications for this project’s specific research aims and data handling needs.

**Repository Contents**

_Steam_ID_Collection.ipynb_
- Collects Steam game IDs ordered by relevance using the Steam store page.
- This notebook is an edited and scoped version of Zhihan Zhu’s Steam Review Scraper approach, adjusted to support this project’s ID acquisition process: https://pypi.org/project/steam-review-scraper/

_Steam_Store_Page.ipynb_
- Uses the collected game IDs to retrieve store-page information.
- This notebook is based on edited code derived from Nik Davis’ implementation, adapted for the project’s data fields and output structure: https://nik-davis.github.io/posts/2019/steam-data-collection/

_Steam_User_Reviews.ipynb_
- Uses the collected game IDs to retrieve user reviews.
- This notebook is based on an edited version of Haotian Xu’s Steam Reviews implementation, adjusted for batch collection, filtering, and dataset formatting: https://pypi.org/project/steam-reviews/

**Data Collection Notes**

The ID collection filter prioritises relevance ordering to capture a broad, contemporary sample of visible games on Steam rather than focusing only on top sellers or new releases - this can be easily changed.

The downstream notebooks are designed to be modular so store metadata and reviews can be collected separately or together depending on the research task.


**Ethical and Responsible Use**

This repository is intended for research use with publicly accessible Steam data.
Users of this code should:
- Respect platform policies and rate limits.
- Avoid collecting or sharing unnecessary personal data.
- Store and distribute datasets in line with institutional ethics requirements and relevant data governance practices.

**Suggested Citation**

If you plan to reuse or build on this pipeline, please cite the associated research outputs that describe the dataset and analysis.

- Byers, T., Gibbs, M., & Nansen, B. (2025). Evaluating Time in Play and Temporal Satisfaction: Time-Centric Language in Video Game User Reviews on Steam. In Conference Proceedings of the 37th Australian Conference on Human–Computer Interaction (OzCHI 2025). https://doi.org/10.1145/3764687.3764693.
- Byers, T., Gibbs, M., & Nansen, B. (2025). Selling Time: Time-Centric Language in Video Game Marketing on Steam. Conference Proceedings of DiGRA 2025 Conference: Games at the Crossroads, 2025(2). https://doi.org/10.26503/dl.v2025i2.2434.
