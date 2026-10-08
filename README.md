# Smart Fan Speed Controller

Fuzzy Logic and Genetic Programming group PBL submission.
L.D. College of Engineering, Ahmedabad. Chemical Engineering, Division A.

## Repository owner
Mahesh Bhaliya, 240280105005. GitHub username: `mbhaliya765-hash`.
Confirmed responsibility: **Testing, graphs and results analysis**.

This repository contains the shared group project. Four account copies support
individual submission requirements. The table records the agreed work allocation.
It does not assert that the entire project was independently authored by each owner.

## Group and work allocation
| Member | Enrollment | GitHub | Confirmed responsibility |
|---|---|---|---|
| Kirtan Siddhapura | 240280105071 | kirtansiddhapura31-collab | Fuzzy controller and rule design |
| Mahesh Bhaliya | 240280105005 | mbhaliya765-hash | Testing, graphs and results analysis |
| Manav Chauhan | 240280105008 | 24chcha008-dotcom | Genetic programming and notebook |
| Haresh Raval | 240280105065 | hareshraval2162-cpu | Report, presentation and video |

## My review and contribution
Run the validation grid and inspect examples.csv, validation.json and the response plots. Explain local decreases and the 16.667 to 83.333 percent output range.

Before publishing, add a short note describing the work you actually completed,
including any changes, verification or explanation you contributed. Commit your
own edits from your own account. The prepared package does not fabricate member
commit history or represent assigned work as completed authorship.

## Run the project
Python 3.10 or later:
```sh
pip install -r requirements.txt
python smart_fan.py --output results
```
Alternatively, open `Smart_Fan.ipynb` and Run All. The notebook is self-contained.
NumPy >=2.0 runs inference and GP. Matplotlib generates the plots.

## Model and actual simulation results
Temperature: 15–40 C. Relative humidity: 20–90 percent.
Nine triangular-set Mamdani rules use min AND, max aggregation and centroid
defuzzification on a 0.1-point output grid. At 30 C / 80% RH, command = 73.113%.
All 1479 validation grid points returned finite bounded results. Local decreases
exist in the surface and are explained in the report.

The separate GP experiment evolves expression trees with a fixed seed of 71,
100 individuals and 40 generations. It uses 85 training and 36 held-out samples.
Held-out RMSE = 9.431 percentage points against simulated fuzzy labels.

Software simulation only. No physical fan measurements, energy savings or human
comfort validation are claimed.

## Deliverables
Python source, executable notebook, result plots and metrics, formatted report,
12-slide PowerPoint and PDF, synthetic narrated MP4 and captions.

## References
https://scikit-fuzzy.github.io/scikit-fuzzy/auto_examples/plot_tipping_problem_newapi.html
https://deap.readthedocs.io/en/stable/tutorials/advanced/gp.html

## Publication links
Video: add the real URL after uploading.
My LinkedIn post: add the real published post URL.
