Hi,

All of the analysis code is in `Explore.ipynb`. Please note that it's not the most robust notebook, towards the end some of the graphs and regression models may produce erroneous results if run multiple times or out of order. Sorry I didn't have time to make the end bits super neat and robust!

Please have a play around with the intervention and baselines reports, try uncommenting some lines to get different reports (by day, time of day, week):
```
intervention_report_df.add_percentage_columns(milk_types, "total").sort_values(by=["day","time_of_day"])
# intervention_report_df.group_by_time_of_day().add_percentage_columns(milk_types, "total")
# intervention_report_df.group_by_week().add_percentage_columns(milk_types, "total")
# intervention_report_df.group_by_day().add_percentage_columns(milk_types, "total")
# intervention_report_df[["coconut", "oat","dairy", "total"]].sum() / intervention_report_df["total"].sum() * 100
```
