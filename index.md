---
layout: default
title: Nayani Ilangakoon
---

<style>
:root {
  --accent-color: #2a7a78;
}

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>{{ page.title }}</title>
    <style>
      :root {
        --accent-color: #2a7a78;
        --accent-dark: #1f5e5c;
        --background-color: #edf3f3;
        --surface-color: #ffffff;
        --text-color: #1f2d3d;
        --muted-text: #5b6b7a;
      }

      *,
      *::before,
      *::after {
        box-sizing: border-box;
      }

      body {
        margin: 0;
        font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
        color: var(--text-color);
        background: var(--background-color);
        line-height: 1.65;
      }

        a {
        color: var(--accent-color);
        text-decoration: none;
        transition: color 0.2s ease, background 0.2s ease, transform 0.2s ease;
      }

        a:hover,
      a:focus {
        color: var(--accent-dark);
      }

        .profile-panel {
        position: relative;
        color: #ffffff;
        background: linear-gradient(160deg, #123939, #2a7a78 55%, #3da8a4);
        padding: 3.5rem 3rem;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        gap: 2.5rem;
        overflow: hidden;
      }

        .profile-panel::before {
        content: "";
        position: absolute;
        inset: 0;
        background: radial-gradient(circle at 20% 20%, rgba(255, 255, 255, 0.28), transparent 55%),
          radial-gradient(circle at 80% 0%, rgba(255, 255, 255, 0.2), transparent 50%),
          linear-gradient(120deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0));
        opacity: 0.9;
        pointer-events: none;
      }

        .profile-panel__inner,
      .profile-panel__nav,
      .profile-panel__note {
        position: relative;
        z-index: 1;
      }

        .profile-panel__inner {
        display: flex;
        flex-direction: column;
        gap: 1.75rem;
      }


        .profile-panel__photo {
        width: 148px;
        height: 148px;
        border-radius: 24px;
        border: 4px solid rgba(255, 255, 255, 0.4);
        box-shadow: 0 18px 36px rgba(6, 41, 44, 0.32);
        object-fit: cover;
      }

        .profile-panel h1 {
        margin: 0;
        font-size: 1.95rem;
        letter-spacing: 0.01em;
      }


        .profile-panel__subtitle {
        font-size: 1.15rem;
        margin: 0;
        max-width: 22ch;
      }

        .profile-panel__description {
        margin: 0;
        opacity: 0.9;
      }

       .profile-panel__cta {
        align-self: flex-start;
        display: inline-flex;
        align-items: center;
        gap: 0.45rem;
        padding: 0.65rem 1.25rem;
        border-radius: 999px;
        background: rgba(255, 255, 255, 0.18);
        color: #ffffff;
        font-weight: 600;
        box-shadow: 0 16px 32px rgba(6, 41, 44, 0.28);
      }

      .profile-panel__cta::after {
        content: "→";
        font-size: 1.1rem;
        transition: transform 0.2s ease;
      }

      .profile-panel__cta:hover::after,
      .profile-panel__cta:focus::after {
        transform: translateX(4px);
      }

      .profile-panel__nav {
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
      }

      .profile-panel__nav-label {
        text-transform: uppercase;
        font-size: 0.75rem;
        letter-spacing: 0.16em;
        color: rgba(255, 255, 255, 0.7);
        font-weight: 600;
      }

      .profile-panel__nav a {
        color: rgba(255, 255, 255, 0.94);
        font-weight: 600;
        position: relative;
        padding-left: 1.4rem;
      }

      .profile-panel__nav a::before {
        content: "";
        position: absolute;
        left: 0;
        top: 50%;
        width: 0.5rem;
        height: 0.5rem;
        border-radius: 999px;
        background: rgba(255, 255, 255, 0.7);
        transform: translateY(-50%);
      }

      .profile-panel__nav a:hover::before,
      .profile-panel__nav a:focus::before {
        background: #ffffff;
      }

      .profile-panel__note {
        margin: 0;
        font-size: 0.85rem;
        color: rgba(255, 255, 255, 0.75);
      }

      .content {
        background: var(--surface-color);
        padding: 3.5rem 3rem;
        margin: 2.5rem;
        margin-left: 2rem;
        border-radius: 32px;
        box-shadow: 0 24px 60px rgba(13, 51, 55, 0.12);
        display: flex;
        flex-direction: column;
        gap: 3.5rem;
        position: relative;
      }

      .content section {
        display: flex;
        flex-direction: column;
        gap: 1rem;
      }

      section h2 {
        margin: 0;
        font-size: 1.9rem;
        font-weight: 700;
        border-bottom: 3px solid rgba(42, 122, 120, 0.15);
        padding-bottom: 0.45rem;
      }

      section p {
        margin: 0;
      }

      .research-intro {
        font-size: 1.05rem;
        color: var(--muted-text);
      }

      ul {
        margin: 0;
        padding-left: 1.4rem;
        color: var(--muted-text);
      }

      .tab-buttons {
        display: flex;
        flex-wrap: wrap;
        gap: 0.75rem;
      }

      .tab-link {
        border: 1px solid var(--accent-color);
        background: #fff;
        color: var(--accent-color);
        padding: 0.6rem 1rem;
        border-radius: 999px;
        font-size: 0.95rem;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.2s ease;
        box-shadow: inset 0 0 0 0 rgba(42, 122, 120, 0.2);
      }

      .tab-link:hover,
      .tab-link:focus {
        background: rgba(42, 122, 120, 0.1);
        outline: none;
      }

      .tab-link.active {
        background: var(--accent-color);
        color: #fff;
        box-shadow: 0 16px 32px rgba(42, 122, 120, 0.25);
      }

      .tab-content {
        display: none;
        border-radius: 18px;
        padding: 1.5rem 1.75rem;
        border: 1px solid rgba(42, 122, 120, 0.15);
        background: linear-gradient(135deg, rgba(42, 122, 120, 0.07), rgba(42, 122, 120, 0.02));
      }

      .tab-content.active {
        display: block;
      }

      .tab-content h3 {
        margin-top: 0;
      }

      .timeline {
        list-style: none;
        padding: 0;
        margin: 0;
        display: grid;
        gap: 1.5rem;
      }

      .timeline__item {
        border-left: 3px solid rgba(42, 122, 120, 0.2);
        padding-left: 1.25rem;
      }

      .timeline__item h3 {
        margin: 0 0 0.35rem;
      }

      .timeline__item span {
        display: inline-block;
        font-size: 0.95rem;
        color: var(--muted-text);
        margin-bottom: 0.5rem;
      }

      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1.75rem;
      }

      .skills-grid h3 {
        margin: 0 0 0.5rem;
      }

      .skills-grid ul {
        padding-left: 1.1rem;
      }

      .site-footer {
        border-top: 1px solid rgba(42, 122, 120, 0.15);
        padding-top: 1.5rem;
        font-size: 0.9rem;
        color: var(--muted-text);
        text-align: center;
      }

      @media (max-width: 1080px) {
        .layout {
          grid-template-columns: minmax(0, 320px) minmax(0, 1fr);
        }

        .profile-panel {
          padding: 3rem 2.5rem;
        }

        .content {
          margin: 2rem;
          margin-left: 1.5rem;
          padding: 3rem 2.5rem;
        }
      }

      @media (max-width: 900px) {
        .layout {
          grid-template-columns: 1fr;
        }

        .profile-panel {
          padding: 2.8rem 2.2rem;
          border-bottom-left-radius: 32px;
          border-bottom-right-radius: 32px;
        }

        .content {
          margin: 0;
          border-radius: 0;
          box-shadow: none;
          padding: 2.75rem 1.8rem 3rem;
        }
      }

      @media (max-width: 600px) {
        .profile-panel {
          padding: 2.5rem 1.6rem;
        }

        .profile-panel__photo {
          width: 128px;
          height: 128px;
        }

        .profile-panel h1 {
          font-size: 1.7rem;
        }

        .profile-panel__subtitle {
          font-size: 1.05rem;
        }

        .content {
          padding: 2.4rem 1.4rem 3rem;
        }

        .tab-buttons {
          flex-direction: column;
        }

        .tab-link {
          width: 100%;
          text-align: center;
        }
      }
    </style>
  </head>
  <body>
    <div class="layout">
      <aside class="profile-panel">
        <div class="profile-panel__inner">
          <img
            src="{{ '/img/IMG_0967.jpg' | relative_url }}"
            alt="Portrait of Nayani Ilangakoon"
            class="profile-panel__photo"
          />
          <h1>Dr. Nayani Ilangakoon</h1>
          <p class="profile-panel__subtitle">
            Remote sensing scientist exploring ecosystem processes across spatial and temporal scales.
          </p>
          <p class="profile-panel__description">
            I develop remote sensing approaches that combine lidar, spectral imagery, and field observations to understand
            ecosystem transformation, carbon trajectories, and resilience in fire-prone landscapes.
          </p>
          <a class="profile-panel__cta" href="https://cires.colorado.edu/people/nayani-ilangakoon">
            Discover CIRES Earth Lab collaborations
          </a>
        </div>
        <nav class="profile-panel__nav" aria-label="Page sections">
          <span class="profile-panel__nav-label">Navigate</span>
          <a href="#research-focus">Research Focus</a>
          <a href="#research-portfolio">Research Portfolio</a>
          <a href="#education">Education</a>
          <a href="#experience">Experience</a>
          <a href="#skills">Skills</a>
        </nav>
        <p class="profile-panel__note">
          Collaborating with the CIRES Earth Lab at the University of Colorado Boulder.
        </p>
      </aside>
      <main class="content">
        <section id="research-focus">
          <h2>Research Focus</h2>
          <p class="research-intro">
            My work centers on translating Earth observation data into actionable science for ecosystem stewardship. I specialize in:
          </p>
          <ul>
            <li>
              Integrating remote sensing technologies (full waveform lidar, multispectral, hyperspectral, SAR, and UAS) to map ecosystem
              structure and function.
            </li>
            <li>
              Modeling wildfire-driven ecosystem transformation and postfire carbon recovery across western North America.
            </li>
            <li>
              Building open, transferable workflows and training resources that make remote sensing accessible to interdisciplinary teams.
            </li>
          </ul>
        </section>

        <section id="research-portfolio">
          <h2>Research Portfolio</h2>
          <p>
            Explore current projects and collaborations. Select a tab to learn more about each research effort.
          </p>
          <div class="tab-buttons" role="tablist" aria-label="Research projects">
            <button
              class="tab-link active"
              role="tab"
              aria-selected="true"
              aria-controls="tab-forest-observatory"
              id="tab-forest-observatory-button"
              data-tab="tab-forest-observatory"
            >
              Open Forest Observatory
            </button>
            <button
              class="tab-link"
              role="tab"
              aria-selected="false"
              aria-controls="tab-ecosystem"
              id="tab-ecosystem-button"
              data-tab="tab-ecosystem"
            >
              Ecosystem Transformation &amp; Carbon
            </button>
            <button
              class="tab-link"
              role="tab"
              aria-selected="false"
              aria-controls="tab-repeat-fires"
              id="tab-repeat-fires-button"
              data-tab="tab-repeat-fires"
            >
              Repeat Fires &amp; Carbon Recovery
            </button>
            <button
              class="tab-link"
              role="tab"
              aria-selected="false"
              aria-controls="tab-fire-impacts"
              id="tab-fire-impacts-button"
              data-tab="tab-fire-impacts"
            >
              Fire Impacts on Forests
            </button>
            <button
              class="tab-link"
              role="tab"
              aria-selected="false"
              aria-controls="tab-postfire-rockies"
              id="tab-postfire-rockies-button"
              data-tab="tab-postfire-rockies"
            >
              Southern Rockies Postfire Carbon
            </button>
            <button
              class="tab-link"
              role="tab"
              aria-selected="false"
              aria-controls="tab-twensday"
              id="tab-twensday-button"
              data-tab="tab-twensday"
            >
              Twensday-03
            </button>
          </div>

          <div
            id="tab-forest-observatory"
            class="tab-content active"
            role="tabpanel"
            aria-labelledby="tab-forest-observatory-button"
          >
            <h3>Open Forest Observatory</h3>
            <p>
              In the Open Forest Observatory initiative we develop forest inventories using individual tree delineations and structural
              attributes derived from unpiloted aerial vehicle (UAV) imagery. Our team tests the transferability of individual tree detection
              models across diverse vegetation conditions and designs training modules that empower scientists to use AI and machine learning
              for ecological applications.
            </p>
          </div>

          <div id="tab-ecosystem" class="tab-content" role="tabpanel" aria-labelledby="tab-ecosystem-button">
            <h3>Ecosystem Transformation &amp; Carbon Consequences</h3>
            <p>
              This project models postfire ecosystem transformation trends and vulnerability in the North Central Climate Adaptation Science
              Center region. By coupling remote sensing time series analyses with known transformation locations and management interventions,
              we evaluate how alternative management strategies influence carbon storage trajectories.
            </p>
          </div>

          <div id="tab-repeat-fires" class="tab-content" role="tabpanel" aria-labelledby="tab-repeat-fires-button">
            <h3>Repeat Fires &amp; Carbon Recovery</h3>
            <p>
              Using a century of fire records alongside GEDI, Sentinel-2, and MODIS observations, I quantify how repeat fire events shape carbon
              potential across western United States forests. The work highlights thresholds in resilience and guides prioritization of
              restoration investments.
            </p>
          </div>

          <div id="tab-fire-impacts" class="tab-content" role="tabpanel" aria-labelledby="tab-fire-impacts-button">
            <h3>Fire Impacts on Forests</h3>
            <p>
              By combining new spaceborne lidar measurements with UAS-based canopy structure, composition, climate, and topographic data, I model
              postfire carbon recovery trajectories. The resulting datasets support scenario planning for land managers balancing carbon
              sequestration and biodiversity goals.
            </p>
          </div>

          <div id="tab-postfire-rockies" class="tab-content" role="tabpanel" aria-labelledby="tab-postfire-rockies-button">
            <h3>Southern Rockies Postfire Carbon Potential</h3>
            <p>
              Field inventories and UAS campaigns across burned scars in the Southern Rockies inform structure-from-motion models that map conifer
              seedling regeneration and growth. The research identifies strategies that accelerate carbon gain and ecosystem resilience following fire.
            </p>
          </div>

          <div id="tab-twensday" class="tab-content" role="tabpanel" aria-labelledby="tab-twensday-button">
            <h3>Twensday-03 Early Warning System</h3>
            <p>
              I lead the Twensday-03 collaboratory to design an early warning system that detects ecosystem transformation tipping points&mdash;including
              forest-to-grass, scrub, and shrubland transitions&mdash;in western U.S. forests. The effort leverages Earth observation data cubes and
              interdisciplinary expertise to anticipate change before it accelerates.
            </p>
          </div>
        </section>

        <section id="education">
          <h2>Education</h2>
          <ul>
            <li><strong>Ph.D. in Geosciences</strong>, Boise State University, Boise, ID, USA (2014&ndash;2020)</li>
            <li><strong>M.S. in Geology</strong>, Bowling Green State University, Bowling Green, OH, USA (2012&ndash;2014)</li>
            <li><strong>B.S. in Geology</strong>, University of Peradeniya, Peradeniya, Sri Lanka (2005&ndash;2009)</li>
          </ul>
        </section>

        <section id="experience">
          <h2>Professional Experience</h2>
          <ul class="timeline">
            <li class="timeline__item">
              <h3>Research Scientist</h3>
              <span>Earth Lab, Cooperative Institute for Research in Environmental Sciences, University of Colorado, Boulder &bull; June 2023&ndash;present</span>
              <p>
                Designs workflows that integrate airborne, spaceborne, and field data to reveal how disturbances reshape carbon storage across landscapes.
              </p>
            </li>
            <li class="timeline__item">
              <h3>Postdoctoral Research Associate</h3>
              <span>Earth Lab, Cooperative Institute for Research in Environmental Sciences, University of Colorado, Boulder &bull; April 2020&ndash;May 2023</span>
              <p>
                Advanced postfire recovery models, co-developed open-source analytics, and mentored students in remote sensing and data science.
              </p>
            </li>
            <li class="timeline__item">
              <h3>Research Assistant</h3>
              <span>Boise State University, Boise, ID, USA &bull; 2016&ndash;2020</span>
              <p>
                Developed and maintained full waveform lidar processing tools, led field data collection, and analyzed airborne datasets to characterize
                vegetation structure, function, and diversity while mentoring graduate and undergraduate researchers.
              </p>
            </li>
            <li class="timeline__item">
              <h3>Research Assistant</h3>
              <span>Bowling Green State University, Bowling Green, OH, USA &bull; 2013&ndash;2014</span>
              <p>
                Oversaw terrestrial laser scanning operations, delivered workshops on TLS data collection, and integrated TLS, field observations, and
                Landsat data to map forest functional traits.
              </p>
            </li>
            <li class="timeline__item">
              <h3>Geologist</h3>
              <span>Geological Survey and Mines Bureau, Sri Lanka &bull; 2011&ndash;2012</span>
              <p>
                Conducted geological and geophysical resource mapping, prepared survey reports, and supported national assessments of mineral deposits.
              </p>
            </li>
          </ul>
        </section>

        <section id="skills">
          <h2>Skills Snapshot</h2>
          <div class="skills-grid">
            <div>
              <h3>Remote Sensing Expertise</h3>
              <ul>
                <li>
                  Technologies: full waveform lidar, discrete return lidar, hyperspectral, multispectral, SAR, and structure-from-motion photogrammetry.
                </li>
                <li>Platforms: satellite, piloted airborne, unpiloted airborne systems (UAS), and terrestrial sensors.</li>
                <li>End-to-end project execution from data collection to product development.</li>
                <li>
                  Domain knowledge spanning forest growth, plant functional traits, wildfires, drought, and carbon sequestration.
                </li>
              </ul>
            </div>
            <div>
              <h3>Geospatial Analytics</h3>
              <ul>
                <li>Spatial analytics, algorithm development, geospatial data management, and rigorous QA/QC.</li>
                <li>
                  Remote sensing big data analytics using high-performance computing, AWS, Google Earth Engine, and Google Colab.
                </li>
              </ul>
            </div>
            <div>
              <h3>Programming</h3>
              <ul>
                <li>
                  Python: Jupyter Notebook, PyCharm, Anaconda, and geospatial libraries including arcpy, GDAL, OGR, shapely, and geopandas.
                </li>
                <li>R: RStudio, R Notebook, and packages such as sf, terra, lidR, and raster.</li>
                <li>MATLAB: signal processing and custom workflows.</li>
              </ul>
            </div>
            <div>
              <h3>Software &amp; Collaboration</h3>
              <ul>
                <li>ENVI, Esri ArcGIS, QGIS, GDAL/OGR, Agisoft Metashape, and Terrasolid.</li>
                <li>
                  Version control and collaboration tools including Git, MS Teams, Trello, Slack, and Google Docs.
                </li>
              </ul>
            </div>
            <div>
              <h3>Field &amp; Outreach</h3>
              <ul>
                <li>
                  Operation of terrestrial laser scanners, UAS (trained pilot), spectroradiometers, LAI-2200, AccuPAR LP-80, and RTK GPS systems.
                </li>
                <li>
                  Experienced in organizing workshops, presenting at conferences, technical writing, and teaching introductory remote sensing and geology.
                </li>
              </ul>
            </div>
          </div>
        </section>

        <footer class="site-footer">
          <p>&copy; {{ site.time | date: '%Y' }} Nayani Ilangakoon. All rights reserved.</p>
        </footer>
      </main>
    </div>

    <script>
      document.addEventListener('DOMContentLoaded', function () {
        var tabButtons = document.querySelectorAll('.tab-link');
        var tabPanels = document.querySelectorAll('.tab-content');

        tabButtons.forEach(function (button) {
          button.addEventListener('click', function () {
            var targetId = button.getAttribute('data-tab');

            tabButtons.forEach(function (btn) {
              btn.classList.remove('active');
              btn.setAttribute('aria-selected', 'false');
            });

            tabPanels.forEach(function (panel) {
              panel.classList.remove('active');
            });

            button.classList.add('active');
            button.setAttribute('aria-selected', 'true');
            var targetPanel = document.getElementById(targetId);
            if (targetPanel) {
              targetPanel.classList.add('active');
            }
          });
        });
      });
    </script>
  </body>
</html>
