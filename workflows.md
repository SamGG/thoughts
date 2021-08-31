# Workflows

Workflows are the skeletons of data processing. A workflow displays the recipe that leads to the results. It ensures the traceability and the reproducibility of the processings.
A workflow consists in many steps. Organizing the results in steps is important for reading the results and transfering/explaining the results to the end user. The results of a step are of two types. The first type targets the expert and permits to get an overview and/or to assay quality. Those files contain text reports, tables, graphics (png, pdf...). The second type targets the processing itself. Those files are input of another step of the workflow and consists in transformed/summarized data.

As the results are stored on disk as files, it is interesting to organize them using the file/directory structure of the operating system of any computer. There are at least 2 possible structures: a linear one and a hierarchical. The linear structure is better when the workflow is linear. The hierarchical structure is better when there could be many branches along the workflow.

To get an overview of the linear structure, take a look at a [discusion at Spectre](https://github.com/ImmuneDynamics/Spectre/discussions/81).

## Linear structure

This is the most common structure that looks like a cooking recipe.

```
010_input/
	FCS files/
	metadata/
020_transformed plots/
030_clustering/
040_annotation/
	FCS files/
	metadata/
050_summary data/
060_info
```

## Hierarchical structure

```
a_input/
	FCS files/
	metadata/
aa_transformed plots/
aaa_clustering/
aaaa_annotation/
	FCS files/
	metadata/
aaaaa_summary data/
aaab_annotation 2/
	FCS files/
	metadata/
aaaba_summary data/
b_info
```

## Points to elaborate

* build an HTML page (index.html) of the directories structure with information (fields below) and direct link to directories and their content (major files)

* add field to each step of the workflow (this sounds like an Electronic Note Book) to insure traceability
  * title
  * description/aim
  * conclusion
  * comment
 
* describe the I/O of any step to propose a list of steps compatible with the current data
