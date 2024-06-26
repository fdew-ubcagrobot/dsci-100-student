---


---

<h1 id="dsci-100-function-reference-sheet-for-r">DSCI 100 function reference sheet for R</h1>
<p>This reference sheet contains the key objects that we use in DSCI 100, and a<br>
brief syntax example for each of the main packages. During the closed book<br>
exams, you will still have access to this page, so get familiar with it already<br>
now. There is no guarantee that every function or parameter in the textbook is<br>
covered here, but if you think there is something missing, please let us know<br>
and we can consider adding it.</p>
<p>Note that we have only described use cases relevant to DSCI 100.<br>
Sometimes we have included the exact parameter name of a function,<br>
e.g. <code>print(x)</code>,<br>
other times we have opted to included a more descriptive name,<br>
e.g. <code>mean(column)</code>.</p>
<h2 id="base-r-operations">Base R Operations</h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>abs(x)</code></td>
<td>Convert numeric value(s) to absolute value</td>
</tr>
<tr>
<td><code>as.data.frame(x)</code></td>
<td>Converts an object to a data frame</td>
</tr>
<tr>
<td><code>as.numeric(x)</code></td>
<td>Converts a variable to a numeric data type</td>
</tr>
<tr>
<td><code>c(1,2,3)</code></td>
<td>Combines values into a vector or list in R</td>
</tr>
<tr>
<td><code>is.na(column)</code></td>
<td>Detect missing (NA) values in a vector or data frame</td>
</tr>
<tr>
<td><code>dim(column)</code></td>
<td>Returns dimensions (rows and columns) of an R object</td>
</tr>
<tr>
<td><code>max(column)</code></td>
<td>Returns maximum value in a numeric vector</td>
</tr>
<tr>
<td><code>mean(column)</code></td>
<td>Returns average value in a numeric vector</td>
</tr>
<tr>
<td><code>median(column)</code></td>
<td>Returns the median value in a numeric vector</td>
</tr>
<tr>
<td><code>min(column)</code></td>
<td>Returns minimum value in a numeric vector</td>
</tr>
<tr>
<td><code>n()</code></td>
<td>Counts the number of rows in a table’s group</td>
</tr>
<tr>
<td><code>names(tbl)</code></td>
<td>Assigns or retrieves names of elements in an R object</td>
</tr>
<tr>
<td><code>ncol(tbl)</code></td>
<td>Returns the number of columns in a matrix/data frame</td>
</tr>
<tr>
<td><code>nrow(tbl)</code></td>
<td>Returns the number of rows in a matrix/data frame</td>
</tr>
<tr>
<td><code>print(x)</code></td>
<td>Displays specified object’s value</td>
</tr>
<tr>
<td><code>round(num, digits)</code></td>
<td>Rounds a number to specified decimals</td>
</tr>
<tr>
<td><code>sd(column)</code></td>
<td>Calculates standard deviation for numeric data</td>
</tr>
<tr>
<td><code>seq(from, to, by)</code></td>
<td>Generates a sequence of numbers</td>
</tr>
<tr>
<td><code>sum(column)</code></td>
<td>Calculates the sum of numeric values in a vector or matrix</td>
</tr>
<tr>
<td><code>sort(df)</code></td>
<td>Sorts a vector or data frame in ascending order</td>
</tr>
<tr>
<td><code>sqrt(num)</code></td>
<td>Computes the square root of a numeric value</td>
</tr>
</tbody>
</table><h2 id="operators">Operators</h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>==</code></td>
<td>Compares two values and returns TRUE if they are equal</td>
</tr>
<tr>
<td><code>%in%</code></td>
<td>Checks if elements on the left side are in the right</td>
</tr>
<tr>
<td><code>!</code></td>
<td>Negates a logical value (!TRUE is FALSE)</td>
</tr>
<tr>
<td><code>&amp;</code></td>
<td>Performs element-wise logical AND operations</td>
</tr>
<tr>
<td><code>|</code></td>
<td>Represents the OR logical operator</td>
</tr>
<tr>
<td><code>|&gt;</code></td>
<td>Pipe operator, which passes data from left to right</td>
</tr>
</tbody>
</table><h2 id="data-reading">Data Reading</h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>download.file(url, destfile)</code></td>
<td>Download a file from the web</td>
</tr>
<tr>
<td><code>read_csv(filepath)</code></td>
<td>Reads comma-separated values into a data frame</td>
</tr>
<tr>
<td><code>read_csv2(filepath)</code></td>
<td>Reads CSV files with semicolon delimiter</td>
</tr>
<tr>
<td><code>read_delim(filepath, delim, skip, col_names)</code></td>
<td>Reads data from a delimited text file</td>
</tr>
<tr>
<td><code>read_excel(filepath)</code></td>
<td>Reads Excel files into R data frames</td>
</tr>
<tr>
<td><code>read_html(filepath)</code></td>
<td>Reads and parses HTML web pages</td>
</tr>
<tr>
<td><code>read_tsv(filepath)</code></td>
<td>Reads tab-separated values into a data frame</td>
</tr>
<tr>
<td><code>write_csv(tbl, filepath)</code></td>
<td>Writes data to a CSV file</td>
</tr>
</tbody>
</table><p>Database functions:</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>collect(database_table)</code></td>
<td>Convert a database table to a tibble</td>
</tr>
<tr>
<td><code>dbConnect(database, dbname)</code></td>
<td>Establishes a connection to a database</td>
</tr>
<tr>
<td><code>dbListTables(dbConnect_object)</code></td>
<td>Lists tables in a database connection</td>
</tr>
<tr>
<td><code>RPostgres::Postgres()</code></td>
<td>Connects to and interacts with PostgreSQL databases</td>
</tr>
<tr>
<td><code>RSQLite::SQLite()</code></td>
<td>Access and manage SQLite database connections</td>
</tr>
<tr>
<td><code>tbl(dbConnect_object, table_name)</code></td>
<td>Creates a data frame from a data source</td>
</tr>
</tbody>
</table><h2 id="data-wrangling">Data Wrangling</h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>across(column_range, function)</code></td>
<td>Apply the given function to each column in the specified column range</td>
</tr>
<tr>
<td><code>arrange(tibble, columns_as_arguments)</code></td>
<td>Order rows by the values of the given columns (default is increasing)</td>
</tr>
<tr>
<td><code>colnames(tbl)</code></td>
<td>Get a list of column names from a tibble</td>
</tr>
<tr>
<td><code>desc(column)</code></td>
<td>Sort a column (or numeric vector) in descending order</td>
</tr>
<tr>
<td><code>everything()</code></td>
<td>Select all variables (used in other functions)</td>
</tr>
<tr>
<td><code>filter(tbl, condition)</code></td>
<td>Keep rows that match a condition</td>
</tr>
<tr>
<td><code>fct_reorder(factor_column, ordering_column, .desc = FALSE)</code></td>
<td>Reorder a column by sorting according to another column</td>
</tr>
<tr>
<td><code>group_by(tbl, columns_as_arguments)</code></td>
<td>Group a tibble by the list of columns provided</td>
</tr>
<tr>
<td><code>map(tbl, function)</code></td>
<td>Apply the given function to each column, creating a list</td>
</tr>
<tr>
<td><code>map_chr(tbl, function)</code></td>
<td>Apply the given function to each column, creating a character vector</td>
</tr>
<tr>
<td><code>map_df(tbl, function)</code></td>
<td>Apply the given function to each column, creating a data frame</td>
</tr>
<tr>
<td><code>mutate(tbl, column_name = ...)</code></td>
<td>Create or modify a column in a tibble</td>
</tr>
<tr>
<td><code>pivot_longer(tbl, column_range, names_to = ..., values_to = ...)</code></td>
<td>Move values from column names to cells</td>
</tr>
<tr>
<td><code>pivot_wider(tbl, names_from = ..., values_from = ...)</code></td>
<td>Move variables from cells to column names</td>
</tr>
<tr>
<td><code>pull(tbl, variable)</code></td>
<td>Extract a single variable from a tibble</td>
</tr>
<tr>
<td><code>rowwise(tbl)</code></td>
<td>Organize a tibble row-by-row for other functions</td>
</tr>
<tr>
<td><code>select(tbl, columns_as_arguments)</code></td>
<td>Keep the given columns</td>
</tr>
<tr>
<td><code>semi_join(tbl, joining_tbl)</code></td>
<td>Keep rows that have matching values in joining_tbl</td>
</tr>
<tr>
<td><code>separate(tbl, column, into, sep)</code></td>
<td>Split values in a column into new columns based on a separator</td>
</tr>
<tr>
<td><code>summarize(tbl, summaries_as_arguments)</code></td>
<td>Compute summary statistics on columns</td>
</tr>
<tr>
<td><code>ungroup(tbl)</code></td>
<td>Undo the effect of group_by()</td>
</tr>
</tbody>
</table><p>Functions used to convert one type to another:</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>as_datetime(formatted_string)</code></td>
<td>Convert a string to a Date object</td>
</tr>
<tr>
<td><code>as_factor(column)</code></td>
<td>Convert a column to a factor / categorical variable</td>
</tr>
<tr>
<td><code>as_tibble(object)</code></td>
<td>Convert an object to a tibble</td>
</tr>
</tbody>
</table><p>Slicing functions:</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>head(tbl)</code></td>
<td>Get the first 6 rows of a tibble</td>
</tr>
<tr>
<td><code>slice(tbl, row_range)</code></td>
<td>Keep rows in the given range</td>
</tr>
<tr>
<td><code>slice_max(tbl, ordering_column, n)</code></td>
<td>Keep the n rows with the largest values of a variable</td>
</tr>
<tr>
<td><code>slice_min(tbl, ordering_column, n)</code></td>
<td>Keep the n rows with the smallest values of a variable</td>
</tr>
<tr>
<td><code>unique(tbl)</code></td>
<td>Delete duplicate rows</td>
</tr>
<tr>
<td><code>tail(tbl)</code></td>
<td>Get the last 6 rows of a tibble</td>
</tr>
</tbody>
</table><p>Functions used to manipulate strings:</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>str_extract(string, pattern)</code></td>
<td>Extract the first substring matching the given pattern</td>
</tr>
<tr>
<td><code>str_replace_all(string, pattern, replacement)</code></td>
<td>Replace all substrings matching the given pattern</td>
</tr>
<tr>
<td><code>tolower(string)</code></td>
<td>Convert a string to all-lowercase</td>
</tr>
<tr>
<td><code>toupper(string)</code></td>
<td>Convert a string to all-uppercase</td>
</tr>
</tbody>
</table><h2 id="visualization">Visualization</h2>
<p>A typical <code>ggplot2</code> syntax for creating a new plot looks something like this:</p>
<pre><code>library(tidyverse)

my_data |&gt; ggplot(aes(x = column1, y = column2)) +
  geom_point()
</code></pre>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>aes(x, y, ...)</code></td>
<td>Specifies how variables in the data are mapped to properties of the plot</td>
</tr>
<tr>
<td><code>element_text(size, colour)</code></td>
<td>Used with <code>theme</code> system to control text size, colour, etc.</td>
</tr>
<tr>
<td><code>facet_grid(rows, cols)</code></td>
<td>Creates matrix panels with plots based on specified rows or cols variable</td>
</tr>
<tr>
<td><code>facet_wrap(facets)</code></td>
<td>Creates a ribbon of panels wrapped in 2d using specified facets</td>
</tr>
<tr>
<td><code>ggmap(map)</code></td>
<td>Used to display visual maps from Google Maps or Stamen Maps</td>
</tr>
<tr>
<td><code>ggpairs(tbl)</code></td>
<td>Plots each variables against all the other variables in a scatterplot matrix</td>
</tr>
<tr>
<td><code>ggplot(tbl, mapping)</code></td>
<td>Initialize a <code>ggplot</code> object, specifying the data and aesthetic mapping for the plot</td>
</tr>
<tr>
<td><code>ggsave(filename, plot)</code></td>
<td>Saves specified plot with given filename to device</td>
</tr>
<tr>
<td><code>ggtitle(title)</code></td>
<td>Adds specified title to the plot</td>
</tr>
<tr>
<td><code>labs(x, y, fill, colour, ...)</code></td>
<td>Modifies labels on the plot, specifying what the new labels should be</td>
</tr>
<tr>
<td><code>scale_color_manual(values)</code></td>
<td>Manually change the colour for plots by specifying the values</td>
</tr>
<tr>
<td><code>scale_fill_brewer(palette)</code></td>
<td>Changes the fill colour palette to the specified palette</td>
</tr>
<tr>
<td><code>scale_fill_distiller(palette)</code></td>
<td>Changes the fill colour palette for continuous scales</td>
</tr>
<tr>
<td><code>scale_x_continuous(limits)</code></td>
<td>Customize x-axis scales for continuous x variables with specified options</td>
</tr>
<tr>
<td><code>scale_x_date(limits, breaks)</code></td>
<td>Customize the x-axis scales for date or time variables in a plot</td>
</tr>
<tr>
<td><code>scale_y_continuous(limits)</code></td>
<td>Customize y-axis scales for continuous y variables with specified options</td>
</tr>
<tr>
<td><code>theme(text)</code></td>
<td>Used to modify the non-data components of the plot with specified options</td>
</tr>
<tr>
<td><code>xlab(label)</code></td>
<td>Modifies the x-axis label to the specified label</td>
</tr>
<tr>
<td><code>xlim(lo, hi)</code></td>
<td>Displays only the specified range on the x-axis of the plot</td>
</tr>
<tr>
<td><code>ylab(label)</code></td>
<td>Modifies the y-axis label to the specified label</td>
</tr>
<tr>
<td><code>ylim(lo, hi)</code></td>
<td>Displays only the specified range on the y-axis of the plot</td>
</tr>
<tr>
<td><code>vars(columns_as_arguments)</code></td>
<td>Choose variables to split a plot on in <code>facet_grid()</code></td>
</tr>
</tbody>
</table><p>Commonly used geometric objects are listed below.</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>geom_abline(slope, intercept)</code></td>
<td>Adds a diagonal line to the plot with specified intercept and slope</td>
</tr>
<tr>
<td><code>geom_bar(stat)</code></td>
<td>Used to create bar graphs with specified <code>stat</code> (often “identity” or “count”)</td>
</tr>
<tr>
<td><code>geom_density()</code></td>
<td>Used to create a smoothened line version of a histogram</td>
</tr>
<tr>
<td><code>geom_freqpoly()</code></td>
<td>Used to create a lined (not smooth) version of a histogram</td>
</tr>
<tr>
<td><code>geom_histogram(bins, binwidth)</code></td>
<td>Creates histogram plots with a specified number of bins and bin width</td>
</tr>
<tr>
<td><code>geom_line()</code></td>
<td>Adds lines to connect data points in the order of the x-axis</td>
</tr>
<tr>
<td><code>geom_point()</code></td>
<td>Used to create a scatterplot graphs</td>
</tr>
<tr>
<td><code>geom_segment(x, y, xend, yend)</code></td>
<td>Draws a straight line on plot connecting (x, y) to (xend, yend)</td>
</tr>
<tr>
<td><code>geom_vline(xintercept)</code></td>
<td>Adds a vertical line to the plot at the specified x-intercept</td>
</tr>
</tbody>
</table><h2 id="modeling">Modeling</h2>
<p>A typical <code>tidymodels</code> workflow looks something like this:</p>
<pre><code>library(tidymodels)

knn_fit &lt;- workflow() |&gt;
  add_recipe(my_recipe) |&gt;
  add_model(knn_spec) |&gt;
  fit(data = my_data)

pred &lt;- predict(knn_fit, new_data)
</code></pre>
<p>The functions below are relevant for Week 7 (<code>classification1</code>) and beyond.</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>add_model(workflow, model_spec)</code></td>
<td>Add a model to a workflow</td>
</tr>
<tr>
<td><code>add_recipe(workflow, model_recipe)</code></td>
<td>Add a recipe to a workflow</td>
</tr>
<tr>
<td><code>add_row(data, col1, col2)</code></td>
<td>Add rows to a dataframe</td>
</tr>
<tr>
<td><code>all_predictors()</code></td>
<td>Select all predictors</td>
</tr>
<tr>
<td><code>bake(recipe, data)</code></td>
<td>Applies the results of prep() into the data</td>
</tr>
<tr>
<td><code>bind_cols(df1, df2)</code></td>
<td>Combine multiple dataframes together</td>
</tr>
<tr>
<td><code>dist(data, method)</code></td>
<td>Computes and returns the distance matrix</td>
</tr>
<tr>
<td><code>as_factor(data, variable)</code></td>
<td>Converts a variable to a factor type</td>
</tr>
<tr>
<td><code>fit(model, data)</code></td>
<td>Add data to a workflow to build a fitted model</td>
</tr>
<tr>
<td><code>predict(fitted_model, new_obs)</code></td>
<td>Predict values based on model and data</td>
</tr>
<tr>
<td><code>prep(recipe)</code></td>
<td>Prepares data for preprocessing</td>
</tr>
<tr>
<td><code>nearest_neighbor(weight_func, neighbors)</code></td>
<td>Specify that the model is K-Nearest-Neighbor</td>
</tr>
<tr>
<td><code>recipe(formula, data)</code></td>
<td>Prepares data for modelling</td>
</tr>
<tr>
<td><code>set_engine(engine)</code></td>
<td>Specify package to fit the model</td>
</tr>
<tr>
<td><code>set_mode(mode)</code></td>
<td>Specify modelling context used</td>
</tr>
<tr>
<td><code>set.seed(n)</code></td>
<td>Make randomization reproducible</td>
</tr>
<tr>
<td><code>step_center(recipe)</code></td>
<td>Center variables in recipe</td>
</tr>
<tr>
<td><code>step_rm(recipe)</code></td>
<td>Removes specified variables</td>
</tr>
<tr>
<td><code>step_scale(recipe)</code></td>
<td>Scale variables in recipe</td>
</tr>
<tr>
<td><code>workflow()</code></td>
<td>Create workflow</td>
</tr>
</tbody>
</table><p>The functions below extend the above table for material in Week 8 (<code>classification2</code>) and beyond.</p>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>apparent(data)</code></td>
<td>Sampling for the apparent error rate</td>
</tr>
<tr>
<td><code>augment(fit, data)</code></td>
<td>Add predictions/residuals/cluster assignments to dataframe</td>
</tr>
<tr>
<td><code>collect_metrics(fitted_model)</code></td>
<td>Aggregate the mean and standard error of the model’s accuracy across the folds</td>
</tr>
<tr>
<td><code>conf_mat(data, truth, estimate)</code></td>
<td>Computes and returns the confusion matrix</td>
</tr>
<tr>
<td><code>fit_resamples(model, resamples)</code></td>
<td>Runs cross-validation on each train/validation split to build a fitted model</td>
</tr>
<tr>
<td><code>glance(fitted_model)</code></td>
<td>Obtain total WSSD of a cluster model</td>
</tr>
<tr>
<td><code>initial_split(data, prop, strata)</code></td>
<td>Splits the data</td>
</tr>
<tr>
<td><code>k_means(num_clusters)</code></td>
<td>Specify that the model is kmeans clustering</td>
</tr>
<tr>
<td><code>kmeans(data, centers, nstart)</code></td>
<td>Runs k-means clustering on the given data for the specified number of clusters and starts</td>
</tr>
<tr>
<td><code>list(objects)</code></td>
<td>Create a list of elements of different types</td>
</tr>
<tr>
<td><code>linear_reg()</code></td>
<td>Specify that the model is linear regression</td>
</tr>
<tr>
<td><code>metrics(data, truth, estimate)</code></td>
<td>Returns the model’s accuracy metrics</td>
</tr>
<tr>
<td><code>testing(data)</code></td>
<td>extract testing data</td>
</tr>
<tr>
<td><code>training(data)</code></td>
<td>extract training data</td>
</tr>
<tr>
<td><code>tune()</code></td>
<td>Tune neighbors</td>
</tr>
<tr>
<td><code>tune_cluster(model, resamples, grid)</code></td>
<td>Run kmeans on multimple resamples of data</td>
</tr>
<tr>
<td><code>tune_grid(model, resamples, grid)</code></td>
<td>Fit the model for each value in a range of parameter values</td>
</tr>
<tr>
<td><code>unlist(list)</code></td>
<td>Convert a list to a vector</td>
</tr>
<tr>
<td><code>unnest(tbl, list_column)</code></td>
<td>Expand a column containing a list of tibbles into rows and columns</td>
</tr>
<tr>
<td><code>vfold_cv(data, v, strata)</code></td>
<td>Perform cross validation</td>
</tr>
</tbody>
</table><h2 id="inference">Inference</h2>

<table>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>quantile(data, percentiles)</code></td>
<td>Finds the specified percentiles in the given data</td>
</tr>
<tr>
<td><code>rep_sample_n(tbl, size, reps, replace)</code></td>
<td>Takes samples of the table according to the size, reps, and replace options</td>
</tr>
<tr>
<td><code>sample_n(tbl, num)</code></td>
<td>Random selects the specified number of rows from the table</td>
</tr>
</tbody>
</table><pre class=" language-r"><code class="prism  language-r">library<span class="token punctuation">(</span>tidyverse<span class="token punctuation">)</span>
library<span class="token punctuation">(</span>tidymodels<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">&lt;-</span> read_csv<span class="token punctuation">(</span><span class="token string">"data/marathon.csv"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  mutate<span class="token punctuation">(</span>
      female <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>female<span class="token punctuation">)</span><span class="token punctuation">,</span>
      footwear <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>footwear<span class="token punctuation">)</span><span class="token punctuation">,</span>
      group <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>group<span class="token punctuation">)</span><span class="token punctuation">,</span>
      injury <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>injury<span class="token punctuation">)</span><span class="token punctuation">,</span>
      mf_di <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>mf_di<span class="token punctuation">)</span><span class="token punctuation">,</span>
      sprint <span class="token operator">=</span> as_factor<span class="token punctuation">(</span>sprint<span class="token punctuation">)</span>
  <span class="token punctuation">)</span>

marathon <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<pre><code>[1mRows: [22m[34m929[39m [1mColumns: [22m[34m13[39m
[36m──[39m [1mColumn specification[22m [36m────────────────────────────────────────────────────────[39m
[1mDelimiter:[22m ","
[32mdbl[39m (13): age, bmi, female, footwear, group, injury, mf_d, mf_di, mf_ti, max...

[36mℹ[39m Use `spec()` to retrieve the full column specification for this data.
[36mℹ[39m Specify the column types or set `show_col_types = FALSE` to quiet this message.
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 13</caption>
<thead>
	<tr><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># use knn to fit the model on everything</span>
k5 <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_mode<span class="token punctuation">(</span><span class="token string">"classification"</span><span class="token punctuation">)</span>
k5
</code></pre>
<pre><code>K-Nearest Neighbor Model Specification (classification)

Main Arguments:
  neighbors = 5
  weight_func = rectangular

Computational engine: kknn 
</code></pre>
<pre class=" language-r"><code class="prism  language-r">r_marathon <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>female <span class="token operator">~</span> max<span class="token punctuation">,</span> data <span class="token operator">=</span> marathon<span class="token punctuation">)</span>
r_marathon
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 1
</code></pre>
<pre class=" language-r"><code class="prism  language-r">f_knn <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_recipe<span class="token punctuation">(</span>r_marathon<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_model<span class="token punctuation">(</span>k5<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    fit<span class="token punctuation">(</span>data <span class="token operator">=</span> marathon<span class="token punctuation">)</span>
f_knn
</code></pre>
<pre><code>══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m nearest_neighbor()

── Preprocessor ────────────────────────────────────────────────────────────────
0 Recipe Steps

── Model ───────────────────────────────────────────────────────────────────────

Call:
kknn::train.kknn(formula = ..y ~ ., data = data, ks = min_rows(5,     data, 5), kernel = ~"rectangular")

Type of response variable: nominal
Minimal misclassification: 0.4036598
Best kernel: rectangular
Best k: 5
</code></pre>
<pre class=" language-r"><code class="prism  language-r">predict<span class="token punctuation">(</span>object <span class="token operator">=</span> f_knn<span class="token punctuation">,</span> new_data <span class="token operator">=</span> marathon<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 1</caption>
<thead>
	<tr><th scope="col">.pred_class</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td></tr>
	<tr><td>1</td></tr>
	<tr><td>0</td></tr>
	<tr><td>0</td></tr>
	<tr><td>0</td></tr>
	<tr><td>0</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 13</caption>
<thead>
	<tr><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">bind_cols<span class="token punctuation">(</span>marathon<span class="token punctuation">,</span> predict<span class="token punctuation">(</span>object <span class="token operator">=</span> f_knn<span class="token punctuation">,</span> new_data <span class="token operator">=</span> marathon<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 14</caption>
<thead>
	<tr><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th><th scope="col">.pred_class</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td><td>0</td></tr>
	<tr><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td><td>1</td></tr>
	<tr><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td><td>0</td></tr>
	<tr><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td><td>0</td></tr>
	<tr><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td><td>0</td></tr>
	<tr><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td><td>0</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span>
    bind_cols<span class="token punctuation">(</span>predict<span class="token punctuation">(</span>f_knn<span class="token punctuation">,</span> marathon<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    count<span class="token punctuation">(</span>female<span class="token punctuation">,</span> .pred_class<span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 4 × 3</caption>
<thead>
	<tr><th scope="col">female</th><th scope="col">.pred_class</th><th scope="col">n</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;int&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td><td>0</td><td>485</td></tr>
	<tr><td>0</td><td>1</td><td>108</td></tr>
	<tr><td>1</td><td>0</td><td>247</td></tr>
	<tr><td>1</td><td>1</td><td> 89</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span>
    bind_cols<span class="token punctuation">(</span>predict<span class="token punctuation">(</span>f_knn<span class="token punctuation">,</span> marathon<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    conf_mat<span class="token punctuation">(</span>female<span class="token punctuation">,</span> .pred_class<span class="token punctuation">)</span>
</code></pre>
<pre><code>          Truth
Prediction   0   1
         0 485 247
         1 108  89
</code></pre>
<pre class=" language-r"><code class="prism  language-r">seq<span class="token punctuation">(</span>from <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">,</span> to <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">,</span> by <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">)</span>
</code></pre>

<ol class="list-inline"><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li><li>6</li><li>7</li><li>8</li><li>9</li><li>10</li></ol>
<pre class=" language-r"><code class="prism  language-r">c<span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span><span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">)</span>
</code></pre>

<ol class="list-inline"><li>1</li><li>3</li><li>5</li><li>7</li><li>9</li><li>20</li></ol>
<pre class=" language-r"><code class="prism  language-r"><span class="token number">1</span><span class="token operator">:</span><span class="token number">5</span>
</code></pre>

<ol class="list-inline"><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li></ol>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># optimal value of k</span>
ks <span class="token operator">&lt;-</span> tibble<span class="token punctuation">(</span>neighbors <span class="token operator">=</span> c<span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
ks
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 1</caption>
<thead>
	<tr><th scope="col">neighbors</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td></tr>
	<tr><td> 3</td></tr>
	<tr><td> 5</td></tr>
	<tr><td> 7</td></tr>
	<tr><td> 9</td></tr>
	<tr><td>20</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">k_multi <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> tune<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_mode<span class="token punctuation">(</span><span class="token string">"classification"</span><span class="token punctuation">)</span>
k_multi
</code></pre>
<pre><code>K-Nearest Neighbor Model Specification (classification)

Main Arguments:
  neighbors = tune()
  weight_func = rectangular

Computational engine: kknn 
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 13</caption>
<thead>
	<tr><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">r_marathon_standard <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>female <span class="token operator">~</span> max<span class="token punctuation">,</span> data <span class="token operator">=</span> marathon<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    step_center<span class="token punctuation">(</span>all_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    step_scale<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
r_marathon_standard
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 1



── Operations 

[36m•[39m Centering for: [34mall_predictors()[39m

[36m•[39m Scaling for: [34mall_numeric_predictors()[39m
</code></pre>
<pre class=" language-r"><code class="prism  language-r">data_vfold <span class="token operator">&lt;-</span> vfold_cv<span class="token punctuation">(</span>marathon<span class="token punctuation">,</span> v <span class="token operator">=</span> <span class="token number">7</span><span class="token punctuation">,</span> strata <span class="token operator">=</span> female<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">results <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_recipe<span class="token punctuation">(</span>r_marathon_standard<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_model<span class="token punctuation">(</span>k_multi<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    tune_grid<span class="token punctuation">(</span>resamples <span class="token operator">=</span> data_vfold<span class="token punctuation">,</span> grid <span class="token operator">=</span> ks<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    collect_metrics<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">accuracies <span class="token operator">&lt;-</span> results <span class="token operator">|</span><span class="token operator">&gt;</span>
   filter<span class="token punctuation">(</span>.metric <span class="token operator">==</span> <span class="token string">"accuracy"</span><span class="token punctuation">)</span>
accuracies
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 7</caption>
<thead>
	<tr><th scope="col">neighbors</th><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">mean</th><th scope="col">n</th><th scope="col">std_err</th><th scope="col">.config</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td><td>accuracy</td><td>binary</td><td>0.5134346</td><td>7</td><td>0.01672894</td><td>Preprocessor1_Model1</td></tr>
	<tr><td> 3</td><td>accuracy</td><td>binary</td><td>0.5855141</td><td>7</td><td>0.01262902</td><td>Preprocessor1_Model2</td></tr>
	<tr><td> 5</td><td>accuracy</td><td>binary</td><td>0.5790694</td><td>7</td><td>0.01248634</td><td>Preprocessor1_Model3</td></tr>
	<tr><td> 7</td><td>accuracy</td><td>binary</td><td>0.5844644</td><td>7</td><td>0.00986704</td><td>Preprocessor1_Model4</td></tr>
	<tr><td> 9</td><td>accuracy</td><td>binary</td><td>0.5973863</td><td>7</td><td>0.01493324</td><td>Preprocessor1_Model5</td></tr>
	<tr><td>20</td><td>accuracy</td><td>binary</td><td>0.6071022</td><td>7</td><td>0.01044979</td><td>Preprocessor1_Model6</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">ggplot<span class="token punctuation">(</span>accuracies<span class="token punctuation">,</span> aes<span class="token punctuation">(</span>x <span class="token operator">=</span> neighbors<span class="token punctuation">,</span> y <span class="token operator">=</span> mean<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span> geom_point<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span> geom_line<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p><img src="output_20_0.svg" alt="svg"></p>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># how do we make sure we can predict well?</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 13</caption>
<thead>
	<tr><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># split the data</span>
set.seed<span class="token punctuation">(</span><span class="token number">4242</span><span class="token punctuation">)</span>

m_split <span class="token operator">&lt;-</span> initial_split<span class="token punctuation">(</span>marathon<span class="token punctuation">,</span> prop <span class="token operator">=</span> <span class="token number">0.75</span><span class="token punctuation">,</span> strata <span class="token operator">=</span> female<span class="token punctuation">)</span>
m_train <span class="token operator">&lt;-</span> training<span class="token punctuation">(</span>m_split<span class="token punctuation">)</span>
m_test <span class="token operator">&lt;-</span> testing<span class="token punctuation">(</span>m_split<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">m_recipe <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>female <span class="token operator">~</span> max<span class="token punctuation">,</span> data <span class="token operator">=</span> marathon<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span> <span class="token comment"># mistake of using full marathon</span>
  step_scale<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  step_center<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

knn_spec <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> <span class="token number">20</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  set_mode<span class="token punctuation">(</span><span class="token string">"classification"</span><span class="token punctuation">)</span>

knn_fit <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  add_recipe<span class="token punctuation">(</span>m_recipe<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  add_model<span class="token punctuation">(</span>knn_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  fit<span class="token punctuation">(</span>data <span class="token operator">=</span> marathon<span class="token punctuation">)</span>

knn_fit
</code></pre>
<pre><code>══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m nearest_neighbor()

── Preprocessor ────────────────────────────────────────────────────────────────
2 Recipe Steps

• step_scale()
• step_center()

── Model ───────────────────────────────────────────────────────────────────────

Call:
kknn::train.kknn(formula = ..y ~ ., data = data, ks = min_rows(20,     data, 5), kernel = ~"rectangular")

Type of response variable: nominal
Minimal misclassification: 0.3659849
Best kernel: rectangular
Best k: 20
</code></pre>
<pre class=" language-r"><code class="prism  language-r">predictions_1 <span class="token operator">&lt;-</span> predict<span class="token punctuation">(</span>knn_fit<span class="token punctuation">,</span> marathon<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  bind_cols<span class="token punctuation">(</span>marathon<span class="token punctuation">)</span>
head<span class="token punctuation">(</span>predictions_1<span class="token punctuation">)</span>

predictions_1 <span class="token percent-operator operator">%&gt;%</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>

</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 14</caption>
<thead>
	<tr><th scope="col">.pred_class</th><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>0</td><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>0</td><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>0</td><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>0</td><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>0</td><td>33</td><td>24.30183</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>14940</td><td>40</td><td>0</td><td>2.824297</td><td>4.150000</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td>0.63293864</td></tr>
	<tr><td>kap     </td><td>binary</td><td>0.07568123</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">recipe_train <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>female <span class="token operator">~</span> max<span class="token punctuation">,</span> data <span class="token operator">=</span> m_train<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span> <span class="token comment"># use train</span>
  step_scale<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  step_center<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

recipe_train

knn_fit_train <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  add_recipe<span class="token punctuation">(</span>recipe_train<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  add_model<span class="token punctuation">(</span>knn_spec<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
  fit<span class="token punctuation">(</span>data <span class="token operator">=</span> m_train<span class="token punctuation">)</span>

knn_fit_train

predictions_2 <span class="token operator">&lt;-</span> predict<span class="token punctuation">(</span>knn_fit_train<span class="token punctuation">,</span> m_train<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span> <span class="token comment"># predict on train</span>
  bind_cols<span class="token punctuation">(</span>m_train<span class="token punctuation">)</span>
head<span class="token punctuation">(</span>predictions_2<span class="token punctuation">)</span>

predictions_2 <span class="token percent-operator operator">%&gt;%</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 1



── Operations 

[36m•[39m Scaling for: [34mall_numeric_predictors()[39m

[36m•[39m Centering for: [34mall_numeric_predictors()[39m




══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m nearest_neighbor()

── Preprocessor ────────────────────────────────────────────────────────────────
2 Recipe Steps

• step_scale()
• step_center()

── Model ───────────────────────────────────────────────────────────────────────

Call:
kknn::train.kknn(formula = ..y ~ ., data = data, ks = min_rows(20,     data, 5), kernel = ~"rectangular")

Type of response variable: nominal
Minimal misclassification: 0.3635057
Best kernel: rectangular
Best k: 20
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 14</caption>
<thead>
	<tr><th scope="col">.pred_class</th><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td><td>35</td><td>23.59232</td><td>0</td><td>2</td><td>1</td><td>2</td><td>42195</td><td>4</td><td>10295</td><td>60</td><td>1</td><td>4.098592</td><td>2.859722</td></tr>
	<tr><td>0</td><td>33</td><td>22.51830</td><td>0</td><td>2</td><td>2</td><td>2</td><td>42195</td><td>3</td><td>12292</td><td>50</td><td>0</td><td>3.432720</td><td>3.414444</td></tr>
	<tr><td>0</td><td>38</td><td>25.56031</td><td>0</td><td>2</td><td>3</td><td>1</td><td>42195</td><td>4</td><td>10980</td><td>65</td><td>0</td><td>3.842896</td><td>3.050000</td></tr>
	<tr><td>0</td><td>34</td><td>22.60793</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>3</td><td>10694</td><td>88</td><td>1</td><td>3.945670</td><td>2.970556</td></tr>
	<tr><td>0</td><td>39</td><td>24.97484</td><td>0</td><td>2</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>13452</td><td>51</td><td>0</td><td>3.136708</td><td>3.736667</td></tr>
	<tr><td>0</td><td>34</td><td>24.57002</td><td>0</td><td>1</td><td>3</td><td>1</td><td>42195</td><td>3</td><td>10747</td><td>75</td><td>1</td><td>3.926212</td><td>2.985278</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td>0.64080460</td></tr>
	<tr><td>kap     </td><td>binary</td><td>0.03333333</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># do it correctly</span>

recipe_train <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>female <span class="token operator">~</span> max<span class="token punctuation">,</span> data <span class="token operator">=</span> marathon<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> <span class="token comment"># use train (good)</span>
  step_scale<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  step_center<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

recipe_train

knn_fit_train <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  add_recipe<span class="token punctuation">(</span>recipe_train<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  add_model<span class="token punctuation">(</span>knn_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  fit<span class="token punctuation">(</span>data <span class="token operator">=</span> m_train<span class="token punctuation">)</span> <span class="token comment"># fit on train (good)</span>

knn_fit_train

predictions_3 <span class="token operator">&lt;-</span> predict<span class="token punctuation">(</span>knn_fit_train<span class="token punctuation">,</span> m_test<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> <span class="token comment"># predict on test (good)</span>
  bind_cols<span class="token punctuation">(</span>m_test<span class="token punctuation">)</span>
head<span class="token punctuation">(</span>predictions_3<span class="token punctuation">)</span>

predictions_3 <span class="token operator">|</span><span class="token operator">&gt;</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 1



── Operations 

[36m•[39m Scaling for: [34mall_numeric_predictors()[39m

[36m•[39m Centering for: [34mall_numeric_predictors()[39m




══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m nearest_neighbor()

── Preprocessor ────────────────────────────────────────────────────────────────
2 Recipe Steps

• step_scale()
• step_center()

── Model ───────────────────────────────────────────────────────────────────────

Call:
kknn::train.kknn(formula = ..y ~ ., data = data, ks = min_rows(20,     data, 5), kernel = ~"rectangular")

Type of response variable: nominal
Minimal misclassification: 0.3635057
Best kernel: rectangular
Best k: 20
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 14</caption>
<thead>
	<tr><th scope="col">.pred_class</th><th scope="col">age</th><th scope="col">bmi</th><th scope="col">female</th><th scope="col">footwear</th><th scope="col">group</th><th scope="col">injury</th><th scope="col">mf_d</th><th scope="col">mf_di</th><th scope="col">mf_ti</th><th scope="col">max</th><th scope="col">sprint</th><th scope="col">mf_s</th><th scope="col">time_hrs</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td><td>24</td><td>22.53944</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>4</td><td>15420</td><td>30</td><td>0</td><td>2.736381</td><td>4.283333</td></tr>
	<tr><td>0</td><td>52</td><td>23.80480</td><td>0</td><td>1</td><td>1</td><td>1</td><td>42195</td><td>4</td><td>13257</td><td>40</td><td>1</td><td>3.182847</td><td>3.682500</td></tr>
	<tr><td>0</td><td>33</td><td>28.20037</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>3</td><td>18484</td><td>15</td><td>0</td><td>2.282785</td><td>5.134444</td></tr>
	<tr><td>0</td><td>27</td><td>20.77415</td><td>1</td><td>2</td><td>2</td><td>1</td><td>42195</td><td>2</td><td>12095</td><td>70</td><td>1</td><td>3.488632</td><td>3.359722</td></tr>
	<tr><td>0</td><td>28</td><td>20.91324</td><td>1</td><td>1</td><td>1</td><td>1</td><td>42195</td><td>2</td><td>10888</td><td>86</td><td>1</td><td>3.875367</td><td>3.024444</td></tr>
	<tr><td>0</td><td>31</td><td>24.52616</td><td>0</td><td>1</td><td>3</td><td>1</td><td>42195</td><td>2</td><td>10778</td><td> 7</td><td>0</td><td>3.914919</td><td>2.993889</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td> 0.63090129</td></tr>
	<tr><td>kap     </td><td>binary</td><td>-0.01038725</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">predictions_1 <span class="token percent-operator operator">%&gt;%</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>

predictions_2 <span class="token percent-operator operator">%&gt;%</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>

predictions_3 <span class="token percent-operator operator">%&gt;%</span>
  metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> female<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred_class<span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td>0.63293864</td></tr>
	<tr><td>kap     </td><td>binary</td><td>0.07568123</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td>0.64080460</td></tr>
	<tr><td>kap     </td><td>binary</td><td>0.03333333</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A tibble: 2 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>accuracy</td><td>binary</td><td> 0.63090129</td></tr>
	<tr><td>kap     </td><td>binary</td><td>-0.01038725</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># regression (knn and linear)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">set.seed<span class="token punctuation">(</span><span class="token number">424242</span><span class="token punctuation">)</span>
m_split <span class="token operator">&lt;-</span> initial_split<span class="token punctuation">(</span>marathon<span class="token punctuation">,</span> prop <span class="token operator">=</span> <span class="token number">0.75</span><span class="token punctuation">,</span> strata <span class="token operator">=</span> female<span class="token punctuation">)</span>
m_train <span class="token operator">&lt;-</span> training<span class="token punctuation">(</span>m_split<span class="token punctuation">)</span>
m_test <span class="token operator">&lt;-</span> testing<span class="token punctuation">(</span>m_split<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon_spec <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> tune<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                 set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                 set_mode<span class="token punctuation">(</span><span class="token string">"regression"</span><span class="token punctuation">)</span>
marathon_spec
</code></pre>
<pre><code>K-Nearest Neighbor Model Specification (regression)

Main Arguments:
  neighbors = tune()
  weight_func = rectangular

Computational engine: kknn 
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span> count<span class="token punctuation">(</span>female<span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 2 × 2</caption>
<thead>
	<tr><th scope="col">female</th><th scope="col">n</th></tr>
	<tr><th scope="col">&lt;fct&gt;</th><th scope="col">&lt;int&gt;</th></tr>
</thead>
<tbody>
	<tr><td>0</td><td>593</td></tr>
	<tr><td>1</td><td>336</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon <span class="token operator">|</span><span class="token operator">&gt;</span> pull<span class="token punctuation">(</span>max<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> mean<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p>53.0012917102799</p>
<pre class=" language-r"><code class="prism  language-r">m_train <span class="token operator">|</span><span class="token operator">&gt;</span> pull<span class="token punctuation">(</span>max<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> mean<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p>52.7594827591667</p>
<pre class=" language-r"><code class="prism  language-r">marathon_recipe <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>time_hrs <span class="token operator">~</span> max <span class="token operator">+</span> female<span class="token punctuation">,</span> data <span class="token operator">=</span> m_train<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                   step_scale<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                   step_center<span class="token punctuation">(</span>all_numeric_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

marathon_recipe
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 2



── Operations 

[36m•[39m Scaling for: [34mall_numeric_predictors()[39m

[36m•[39m Centering for: [34mall_numeric_predictors()[39m
</code></pre>
<pre class=" language-r"><code class="prism  language-r">gridvals <span class="token operator">&lt;-</span> tibble<span class="token punctuation">(</span>neighbors <span class="token operator">=</span> seq<span class="token punctuation">(</span>from <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">,</span> to <span class="token operator">=</span> <span class="token number">41</span><span class="token punctuation">,</span> by <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
gridvals
</code></pre>
<table class="dataframe">
<caption>A tibble: 5 × 1</caption>
<thead>
	<tr><th scope="col">neighbors</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td></tr>
	<tr><td>11</td></tr>
	<tr><td>21</td></tr>
	<tr><td>31</td></tr>
	<tr><td>41</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon_vfold <span class="token operator">&lt;-</span> vfold_cv<span class="token punctuation">(</span>m_train<span class="token punctuation">,</span> v <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">,</span> strata <span class="token operator">=</span> time_hrs<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">marathon_workflow <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                     add_recipe<span class="token punctuation">(</span>marathon_recipe<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                     add_model<span class="token punctuation">(</span>marathon_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                     tune_grid<span class="token punctuation">(</span>resamples <span class="token operator">=</span> marathon_vfold<span class="token punctuation">,</span> grid <span class="token operator">=</span> gridvals<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                     collect_metrics<span class="token punctuation">(</span><span class="token punctuation">)</span>
marathon_workflow
</code></pre>
<table class="dataframe">
<caption>A tibble: 10 × 7</caption>
<thead>
	<tr><th scope="col">neighbors</th><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">mean</th><th scope="col">n</th><th scope="col">std_err</th><th scope="col">.config</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td><td>rmse</td><td>standard</td><td>0.8189310</td><td>5</td><td>0.01243811</td><td>Preprocessor1_Model1</td></tr>
	<tr><td> 1</td><td>rsq </td><td>standard</td><td>0.1484223</td><td>5</td><td>0.01008181</td><td>Preprocessor1_Model1</td></tr>
	<tr><td>11</td><td>rmse</td><td>standard</td><td>0.5573217</td><td>5</td><td>0.01871256</td><td>Preprocessor1_Model2</td></tr>
	<tr><td>11</td><td>rsq </td><td>standard</td><td>0.3894622</td><td>5</td><td>0.01862499</td><td>Preprocessor1_Model2</td></tr>
	<tr><td>21</td><td>rmse</td><td>standard</td><td>0.5505424</td><td>5</td><td>0.01586727</td><td>Preprocessor1_Model3</td></tr>
	<tr><td>21</td><td>rsq </td><td>standard</td><td>0.4023609</td><td>5</td><td>0.01493617</td><td>Preprocessor1_Model3</td></tr>
	<tr><td>31</td><td>rmse</td><td>standard</td><td>0.5464866</td><td>5</td><td>0.01708139</td><td>Preprocessor1_Model4</td></tr>
	<tr><td>31</td><td>rsq </td><td>standard</td><td>0.4084444</td><td>5</td><td>0.01368831</td><td>Preprocessor1_Model4</td></tr>
	<tr><td>41</td><td>rmse</td><td>standard</td><td>0.5459294</td><td>5</td><td>0.01805168</td><td>Preprocessor1_Model5</td></tr>
	<tr><td>41</td><td>rsq </td><td>standard</td><td>0.4096833</td><td>5</td><td>0.01456921</td><td>Preprocessor1_Model5</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon_acc <span class="token operator">&lt;-</span> marathon_workflow <span class="token operator">|</span><span class="token operator">&gt;</span>
    filter<span class="token punctuation">(</span>.metric <span class="token operator">==</span> <span class="token string">'rmse'</span><span class="token punctuation">)</span>
marathon_acc
</code></pre>
<table class="dataframe">
<caption>A tibble: 5 × 7</caption>
<thead>
	<tr><th scope="col">neighbors</th><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">mean</th><th scope="col">n</th><th scope="col">std_err</th><th scope="col">.config</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td><td>rmse</td><td>standard</td><td>0.8189310</td><td>5</td><td>0.01243811</td><td>Preprocessor1_Model1</td></tr>
	<tr><td>11</td><td>rmse</td><td>standard</td><td>0.5573217</td><td>5</td><td>0.01871256</td><td>Preprocessor1_Model2</td></tr>
	<tr><td>21</td><td>rmse</td><td>standard</td><td>0.5505424</td><td>5</td><td>0.01586727</td><td>Preprocessor1_Model3</td></tr>
	<tr><td>31</td><td>rmse</td><td>standard</td><td>0.5464866</td><td>5</td><td>0.01708139</td><td>Preprocessor1_Model4</td></tr>
	<tr><td>41</td><td>rmse</td><td>standard</td><td>0.5459294</td><td>5</td><td>0.01805168</td><td>Preprocessor1_Model5</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon_acc <span class="token operator">|</span><span class="token operator">&gt;</span>
 filter<span class="token punctuation">(</span>mean <span class="token operator">==</span> min<span class="token punctuation">(</span>mean<span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 1 × 7</caption>
<thead>
	<tr><th scope="col">neighbors</th><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">mean</th><th scope="col">n</th><th scope="col">std_err</th><th scope="col">.config</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><td>41</td><td>rmse</td><td>standard</td><td>0.5459294</td><td>5</td><td>0.01805168</td><td>Preprocessor1_Model5</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">marathon_acc <span class="token operator">|</span><span class="token operator">&gt;</span>
    slice_min<span class="token punctuation">(</span>mean<span class="token punctuation">,</span> n<span class="token operator">=</span><span class="token number">1</span><span class="token punctuation">)</span> 
</code></pre>
<table class="dataframe">
<caption>A tibble: 1 × 7</caption>
<thead>
	<tr><th scope="col">neighbors</th><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">mean</th><th scope="col">n</th><th scope="col">std_err</th><th scope="col">.config</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><td>41</td><td>rmse</td><td>standard</td><td>0.5459294</td><td>5</td><td>0.01805168</td><td>Preprocessor1_Model5</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">k_best <span class="token operator">&lt;-</span> marathon_acc <span class="token operator">|</span><span class="token operator">&gt;</span>
  filter<span class="token punctuation">(</span>mean <span class="token operator">==</span> min<span class="token punctuation">(</span>mean<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
  pull<span class="token punctuation">(</span>neighbors<span class="token punctuation">)</span>
k_best
</code></pre>
<p>41</p>
<pre class=" language-r"><code class="prism  language-r">marathon_best_spec <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> k_best<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                            set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                            set_mode<span class="token punctuation">(</span><span class="token string">"regression"</span><span class="token punctuation">)</span>

marathon_best_fit <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        add_recipe<span class="token punctuation">(</span>marathon_recipe<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        add_model<span class="token punctuation">(</span>marathon_best_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        fit<span class="token punctuation">(</span>data <span class="token operator">=</span> m_train<span class="token punctuation">)</span>

marathon_summary <span class="token operator">&lt;-</span> marathon_best_fit <span class="token operator">|</span><span class="token operator">&gt;</span> 
                       predict<span class="token punctuation">(</span>m_test<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                       bind_cols<span class="token punctuation">(</span>m_test<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                       metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> time_hrs<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred<span class="token punctuation">)</span> 
marathon_summary
</code></pre>
<table class="dataframe">
<caption>A tibble: 3 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>rmse</td><td>standard</td><td>0.5998920</td></tr>
	<tr><td>rsq </td><td>standard</td><td>0.4184801</td></tr>
	<tr><td>mae </td><td>standard</td><td>0.4332147</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># mess up train/test</span>
marathon_best_spec <span class="token operator">&lt;-</span> nearest_neighbor<span class="token punctuation">(</span>weight_func <span class="token operator">=</span> <span class="token string">"rectangular"</span><span class="token punctuation">,</span> neighbors <span class="token operator">=</span> k_best<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                            set_engine<span class="token punctuation">(</span><span class="token string">"kknn"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                            set_mode<span class="token punctuation">(</span><span class="token string">"regression"</span><span class="token punctuation">)</span>

marathon_best_fit <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        add_recipe<span class="token punctuation">(</span>marathon_recipe<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        add_model<span class="token punctuation">(</span>marathon_best_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                        fit<span class="token punctuation">(</span>data <span class="token operator">=</span> m_train<span class="token punctuation">)</span>

marathon_summary <span class="token operator">&lt;-</span> marathon_best_fit <span class="token operator">|</span><span class="token operator">&gt;</span> 
                       predict<span class="token punctuation">(</span>m_train<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                       bind_cols<span class="token punctuation">(</span>m_train<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
                       metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> time_hrs<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred<span class="token punctuation">)</span> 
marathon_summary
<span class="token comment"># rmse lower, (so a bit better. but artificial)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 3 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>rmse</td><td>standard</td><td>0.5331159</td></tr>
	<tr><td>rsq </td><td>standard</td><td>0.4355620</td></tr>
	<tr><td>mae </td><td>standard</td><td>0.4054456</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">lm_spec <span class="token operator">&lt;-</span> linear_reg<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_engine<span class="token punctuation">(</span><span class="token string">"lm"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    set_mode<span class="token punctuation">(</span><span class="token string">"regression"</span><span class="token punctuation">)</span>

<span class="token comment"># marathon_recipe</span>
marathon_recipe <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span>time_hrs <span class="token operator">~</span> max <span class="token operator">+</span> female<span class="token punctuation">,</span> data <span class="token operator">=</span> m_train<span class="token punctuation">)</span>

marathon_recipe

lm_mod <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_recipe<span class="token punctuation">(</span>marathon_recipe<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_model<span class="token punctuation">(</span>lm_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    fit<span class="token punctuation">(</span>data <span class="token operator">=</span> m_train<span class="token punctuation">)</span>
lm_mod
</code></pre>
<pre><code>[36m──[39m [1mRecipe[22m [36m──────────────────────────────────────────────────────────────────────[39m



── Inputs 

Number of variables by role

outcome:   1
predictor: 2




══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m linear_reg()

── Preprocessor ────────────────────────────────────────────────────────────────
0 Recipe Steps

── Model ───────────────────────────────────────────────────────────────────────

Call:
stats::lm(formula = ..y ~ ., data = data)

Coefficients:
(Intercept)          max      female1  
    4.65596     -0.02026      0.37418  
</code></pre>
<pre class=" language-r"><code class="prism  language-r">lm_mod <span class="token operator">|</span><span class="token operator">&gt;</span> 
    predict<span class="token punctuation">(</span>m_test<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    bind_cols<span class="token punctuation">(</span>m_test<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    metrics<span class="token punctuation">(</span>truth <span class="token operator">=</span> time_hrs<span class="token punctuation">,</span> estimate <span class="token operator">=</span> .pred<span class="token punctuation">)</span> 
</code></pre>
<table class="dataframe">
<caption>A tibble: 3 × 3</caption>
<thead>
	<tr><th scope="col">.metric</th><th scope="col">.estimator</th><th scope="col">.estimate</th></tr>
	<tr><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;chr&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>rmse</td><td>standard</td><td>0.6097583</td></tr>
	<tr><td>rsq </td><td>standard</td><td>0.3980943</td></tr>
	<tr><td>mae </td><td>standard</td><td>0.4446058</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># clustering</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">mtcars_subset <span class="token operator">&lt;-</span> mtcars <span class="token percent-operator operator">%&gt;%</span>
  select<span class="token punctuation">(</span>mpg<span class="token punctuation">,</span> disp<span class="token punctuation">,</span> hp<span class="token punctuation">,</span> wt<span class="token punctuation">)</span>
mtcars_subset <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A data.frame: 6 × 4</caption>
<thead>
	<tr><th></th><th scope="col">mpg</th><th scope="col">disp</th><th scope="col">hp</th><th scope="col">wt</th></tr>
	<tr><th></th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">Mazda RX4</th><td>21.0</td><td>160</td><td>110</td><td>2.620</td></tr>
	<tr><th scope="row">Mazda RX4 Wag</th><td>21.0</td><td>160</td><td>110</td><td>2.875</td></tr>
	<tr><th scope="row">Datsun 710</th><td>22.8</td><td>108</td><td> 93</td><td>2.320</td></tr>
	<tr><th scope="row">Hornet 4 Drive</th><td>21.4</td><td>258</td><td>110</td><td>3.215</td></tr>
	<tr><th scope="row">Hornet Sportabout</th><td>18.7</td><td>360</td><td>175</td><td>3.440</td></tr>
	<tr><th scope="row">Valiant</th><td>18.1</td><td>225</td><td>105</td><td>3.460</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">library<span class="token punctuation">(</span>tidyclust<span class="token punctuation">)</span>
r_clust <span class="token operator">&lt;-</span> recipe<span class="token punctuation">(</span><span class="token operator">~</span> .<span class="token punctuation">,</span> data <span class="token operator">=</span> mtcars_subset<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    step_scale<span class="token punctuation">(</span>all_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    step_center<span class="token punctuation">(</span>all_predictors<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

s_clust <span class="token operator">&lt;-</span> k_means<span class="token punctuation">(</span>num_clusters <span class="token operator">=</span> <span class="token number">4</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> <span class="token comment"># kmeans come from tidyclust</span>
    set_engine<span class="token punctuation">(</span><span class="token string">"stats"</span><span class="token punctuation">)</span>

c_cars <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_recipe<span class="token punctuation">(</span>r_clust<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_model<span class="token punctuation">(</span>s_clust<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    fit<span class="token punctuation">(</span>data <span class="token operator">=</span> mtcars_subset<span class="token punctuation">)</span>

c_cars
</code></pre>
<pre><code>══ Workflow [trained] ══════════════════════════════════════════════════════════
[3mPreprocessor:[23m Recipe
[3mModel:[23m k_means()

── Preprocessor ────────────────────────────────────────────────────────────────
2 Recipe Steps

• step_scale()
• step_center()

── Model ───────────────────────────────────────────────────────────────────────
K-means clustering with 4 clusters of sizes 12, 7, 7, 6

Cluster means:
         mpg       disp         hp         wt
4  0.1384407 -0.5707543 -0.5448163 -0.2454544
3 -0.5483556  0.6850701  0.3400164  0.4816984
1 -1.1077479  1.2897470  1.4839092  1.1166629
2  1.6552394 -1.1624447 -1.0382807 -1.3738462

Clustering vector:
 [1] 1 1 1 1 2 1 3 1 1 1 1 2 2 2 3 3 3 4 4 4 1 2 2 3 2 4 4 4 3 1 3 1

Within cluster sum of squares by cluster:
[1]  5.890043  1.961321 10.922714  2.262541
 (between_SS / total_SS =  83.0 %)

Available components:

[1] "cluster"      "centers"      "totss"        "withinss"     "tot.withinss"
[6] "betweenss"    "size"         "iter"         "ifault"      
</code></pre>
<pre class=" language-r"><code class="prism  language-r">mtcars_subset <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A data.frame: 6 × 4</caption>
<thead>
	<tr><th></th><th scope="col">mpg</th><th scope="col">disp</th><th scope="col">hp</th><th scope="col">wt</th></tr>
	<tr><th></th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">Mazda RX4</th><td>21.0</td><td>160</td><td>110</td><td>2.620</td></tr>
	<tr><th scope="row">Mazda RX4 Wag</th><td>21.0</td><td>160</td><td>110</td><td>2.875</td></tr>
	<tr><th scope="row">Datsun 710</th><td>22.8</td><td>108</td><td> 93</td><td>2.320</td></tr>
	<tr><th scope="row">Hornet 4 Drive</th><td>21.4</td><td>258</td><td>110</td><td>3.215</td></tr>
	<tr><th scope="row">Hornet Sportabout</th><td>18.7</td><td>360</td><td>175</td><td>3.440</td></tr>
	<tr><th scope="row">Valiant</th><td>18.1</td><td>225</td><td>105</td><td>3.460</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">clustered_cars <span class="token operator">&lt;-</span> augment<span class="token punctuation">(</span>c_cars<span class="token punctuation">,</span> mtcars_subset<span class="token punctuation">)</span> <span class="token comment"># really similar to bind_cols we did before</span>
clustered_cars <span class="token operator">|</span><span class="token operator">&gt;</span> head<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<table class="dataframe">
<caption>A tibble: 6 × 5</caption>
<thead>
	<tr><th scope="col">mpg</th><th scope="col">disp</th><th scope="col">hp</th><th scope="col">wt</th><th scope="col">.pred_cluster</th></tr>
	<tr><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;fct&gt;</th></tr>
</thead>
<tbody>
	<tr><td>21.0</td><td>160</td><td>110</td><td>2.620</td><td>Cluster_1</td></tr>
	<tr><td>21.0</td><td>160</td><td>110</td><td>2.875</td><td>Cluster_1</td></tr>
	<tr><td>22.8</td><td>108</td><td> 93</td><td>2.320</td><td>Cluster_1</td></tr>
	<tr><td>21.4</td><td>258</td><td>110</td><td>3.215</td><td>Cluster_1</td></tr>
	<tr><td>18.7</td><td>360</td><td>175</td><td>3.440</td><td>Cluster_2</td></tr>
	<tr><td>18.1</td><td>225</td><td>105</td><td>3.460</td><td>Cluster_1</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">ggplot<span class="token punctuation">(</span>clustered_cars<span class="token punctuation">,</span> aes<span class="token punctuation">(</span>x <span class="token operator">=</span> hp<span class="token punctuation">,</span> y <span class="token operator">=</span> mpg<span class="token punctuation">,</span> colour <span class="token operator">=</span> .pred_cluster<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span>
  geom_point<span class="token punctuation">(</span>alpha <span class="token operator">=</span> <span class="token number">0.5</span><span class="token punctuation">,</span> size <span class="token operator">=</span> <span class="token number">2</span><span class="token punctuation">)</span>
</code></pre>
<p><img src="output_52_0.svg" alt="svg"></p>
<pre class=" language-r"><code class="prism  language-r">
</code></pre>
<pre class=" language-r"><code class="prism  language-r">ks <span class="token operator">&lt;-</span> tibble<span class="token punctuation">(</span>num_clusters <span class="token operator">=</span> <span class="token number">1</span><span class="token operator">:</span><span class="token number">10</span><span class="token punctuation">)</span>

new_spec <span class="token operator">&lt;-</span> k_means<span class="token punctuation">(</span>num_clusters <span class="token operator">=</span> tune<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> set_engine<span class="token punctuation">(</span><span class="token string">"stats"</span><span class="token punctuation">,</span> nstart<span class="token operator">=</span><span class="token number">10</span><span class="token punctuation">)</span>

elbow_stats <span class="token operator">&lt;-</span> workflow<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_recipe<span class="token punctuation">(</span>r_clust<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    add_model<span class="token punctuation">(</span>new_spec<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    tune_cluster<span class="token punctuation">(</span>resamples <span class="token operator">=</span> apparent<span class="token punctuation">(</span>mtcars_subset<span class="token punctuation">)</span><span class="token punctuation">,</span> grid <span class="token operator">=</span> ks<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span> <span class="token comment"># really similar to fit resamples when doing cv</span>
    collect_metrics<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>`
    filter<span class="token punctuation">(</span>.metric <span class="token operator">==</span> <span class="token string">"sse_within_total"</span><span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    mutate<span class="token punctuation">(</span>total_WSSD <span class="token operator">=</span> mean<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    select<span class="token punctuation">(</span>num_clusters<span class="token punctuation">,</span> total_WSSD<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">?apparent
</code></pre>
<table><tbody><tr><td>apparent {rsample}</td><td>R Documentation</td></tr></tbody></table>
<h2 id="apparent">Sampling for the Apparent Error Rate</h2>
<h3>Description</h3>
<p>When building a model on a data set and re-predicting the same data, the
performance estimate from those predictions is often called the
"apparent" performance of the model. This estimate can be wildly
optimistic. "Apparent sampling" here means that the analysis and
assessment samples are the same. These resamples are sometimes used in
the analysis of bootstrap samples and should otherwise be
avoided like old sushi.
</p>
<h3>Usage</h3>
<pre><code class="language-R">apparent(data, ...)
</code></pre>
<h3>Arguments</h3>
<table>
<tbody><tr><td><code id="apparent_:_data">data</code></td>
<td>
<p>A data frame.</p>
</td></tr>
<tr><td><code id="apparent_:_...">...</code></td>
<td>
<p>These dots are for future extensions and must be empty.</p>
</td></tr>
</tbody></table>
<h3>Value</h3>
<p>A tibble with a single row and classes <code>apparent</code>,
<code>rset</code>, <code>tbl_df</code>, <code>tbl</code>, and <code>data.frame</code>. The
results include a column for the data split objects and one column
called <code>id</code> that has a character string with the resample identifier.
</p>
<h3>Examples</h3>
<pre><code class="language-R">apparent(mtcars)
</code></pre>
<hr><div>[Package <em>rsample</em> version 1.2.0 ]</div>

<pre class=" language-r"><code class="prism  language-r">elbow_stats
</code></pre>
<table class="dataframe">
<caption>A tibble: 10 × 2</caption>
<thead>
	<tr><th scope="col">num_clusters</th><th scope="col">total_WSSD</th></tr>
	<tr><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td><td>124.000000</td></tr>
	<tr><td> 2</td><td> 46.072608</td></tr>
	<tr><td> 3</td><td> 29.402405</td></tr>
	<tr><td> 4</td><td> 18.369057</td></tr>
	<tr><td> 5</td><td> 12.209820</td></tr>
	<tr><td> 6</td><td>  9.581504</td></tr>
	<tr><td> 7</td><td>  8.444016</td></tr>
	<tr><td> 8</td><td>  7.184407</td></tr>
	<tr><td> 9</td><td>  6.273651</td></tr>
	<tr><td>10</td><td>  5.432449</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">ggplot<span class="token punctuation">(</span>elbow_stats<span class="token punctuation">,</span> aes<span class="token punctuation">(</span>x <span class="token operator">=</span> num_clusters<span class="token punctuation">,</span> y <span class="token operator">=</span> total_WSSD<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span>
  geom_point<span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">+</span>
  geom_line<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p><img src="output_57_0.svg" alt="svg"></p>
<pre class=" language-r"><code class="prism  language-r"><span class="token comment"># inference</span>
</code></pre>
<pre class=" language-r"><code class="prism  language-r">library<span class="token punctuation">(</span>tidyverse<span class="token punctuation">)</span>
library<span class="token punctuation">(</span>tidymodels<span class="token punctuation">)</span>

<span class="token comment"># inference example -----</span>

mtcars

mtcars_sample <span class="token operator">&lt;-</span> mtcars <span class="token operator">|</span><span class="token operator">&gt;</span> sample_n<span class="token punctuation">(</span>size <span class="token operator">=</span> <span class="token number">16</span><span class="token punctuation">)</span>

mtcars_sample

</code></pre>
<table class="dataframe">
<caption>A data.frame: 32 × 11</caption>
<thead>
	<tr><th></th><th scope="col">mpg</th><th scope="col">cyl</th><th scope="col">disp</th><th scope="col">hp</th><th scope="col">drat</th><th scope="col">wt</th><th scope="col">qsec</th><th scope="col">vs</th><th scope="col">am</th><th scope="col">gear</th><th scope="col">carb</th></tr>
	<tr><th></th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">Mazda RX4</th><td>21.0</td><td>6</td><td>160.0</td><td>110</td><td>3.90</td><td>2.620</td><td>16.46</td><td>0</td><td>1</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Mazda RX4 Wag</th><td>21.0</td><td>6</td><td>160.0</td><td>110</td><td>3.90</td><td>2.875</td><td>17.02</td><td>0</td><td>1</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Datsun 710</th><td>22.8</td><td>4</td><td>108.0</td><td> 93</td><td>3.85</td><td>2.320</td><td>18.61</td><td>1</td><td>1</td><td>4</td><td>1</td></tr>
	<tr><th scope="row">Hornet 4 Drive</th><td>21.4</td><td>6</td><td>258.0</td><td>110</td><td>3.08</td><td>3.215</td><td>19.44</td><td>1</td><td>0</td><td>3</td><td>1</td></tr>
	<tr><th scope="row">Hornet Sportabout</th><td>18.7</td><td>8</td><td>360.0</td><td>175</td><td>3.15</td><td>3.440</td><td>17.02</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">Valiant</th><td>18.1</td><td>6</td><td>225.0</td><td>105</td><td>2.76</td><td>3.460</td><td>20.22</td><td>1</td><td>0</td><td>3</td><td>1</td></tr>
	<tr><th scope="row">Duster 360</th><td>14.3</td><td>8</td><td>360.0</td><td>245</td><td>3.21</td><td>3.570</td><td>15.84</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Merc 240D</th><td>24.4</td><td>4</td><td>146.7</td><td> 62</td><td>3.69</td><td>3.190</td><td>20.00</td><td>1</td><td>0</td><td>4</td><td>2</td></tr>
	<tr><th scope="row">Merc 230</th><td>22.8</td><td>4</td><td>140.8</td><td> 95</td><td>3.92</td><td>3.150</td><td>22.90</td><td>1</td><td>0</td><td>4</td><td>2</td></tr>
	<tr><th scope="row">Merc 280</th><td>19.2</td><td>6</td><td>167.6</td><td>123</td><td>3.92</td><td>3.440</td><td>18.30</td><td>1</td><td>0</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Merc 280C</th><td>17.8</td><td>6</td><td>167.6</td><td>123</td><td>3.92</td><td>3.440</td><td>18.90</td><td>1</td><td>0</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Merc 450SE</th><td>16.4</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>4.070</td><td>17.40</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Merc 450SL</th><td>17.3</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>3.730</td><td>17.60</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Merc 450SLC</th><td>15.2</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>3.780</td><td>18.00</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Cadillac Fleetwood</th><td>10.4</td><td>8</td><td>472.0</td><td>205</td><td>2.93</td><td>5.250</td><td>17.98</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Lincoln Continental</th><td>10.4</td><td>8</td><td>460.0</td><td>215</td><td>3.00</td><td>5.424</td><td>17.82</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Chrysler Imperial</th><td>14.7</td><td>8</td><td>440.0</td><td>230</td><td>3.23</td><td>5.345</td><td>17.42</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Fiat 128</th><td>32.4</td><td>4</td><td> 78.7</td><td> 66</td><td>4.08</td><td>2.200</td><td>19.47</td><td>1</td><td>1</td><td>4</td><td>1</td></tr>
	<tr><th scope="row">Honda Civic</th><td>30.4</td><td>4</td><td> 75.7</td><td> 52</td><td>4.93</td><td>1.615</td><td>18.52</td><td>1</td><td>1</td><td>4</td><td>2</td></tr>
	<tr><th scope="row">Toyota Corolla</th><td>33.9</td><td>4</td><td> 71.1</td><td> 65</td><td>4.22</td><td>1.835</td><td>19.90</td><td>1</td><td>1</td><td>4</td><td>1</td></tr>
	<tr><th scope="row">Toyota Corona</th><td>21.5</td><td>4</td><td>120.1</td><td> 97</td><td>3.70</td><td>2.465</td><td>20.01</td><td>1</td><td>0</td><td>3</td><td>1</td></tr>
	<tr><th scope="row">Dodge Challenger</th><td>15.5</td><td>8</td><td>318.0</td><td>150</td><td>2.76</td><td>3.520</td><td>16.87</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">AMC Javelin</th><td>15.2</td><td>8</td><td>304.0</td><td>150</td><td>3.15</td><td>3.435</td><td>17.30</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">Camaro Z28</th><td>13.3</td><td>8</td><td>350.0</td><td>245</td><td>3.73</td><td>3.840</td><td>15.41</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Pontiac Firebird</th><td>19.2</td><td>8</td><td>400.0</td><td>175</td><td>3.08</td><td>3.845</td><td>17.05</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">Fiat X1-9</th><td>27.3</td><td>4</td><td> 79.0</td><td> 66</td><td>4.08</td><td>1.935</td><td>18.90</td><td>1</td><td>1</td><td>4</td><td>1</td></tr>
	<tr><th scope="row">Porsche 914-2</th><td>26.0</td><td>4</td><td>120.3</td><td> 91</td><td>4.43</td><td>2.140</td><td>16.70</td><td>0</td><td>1</td><td>5</td><td>2</td></tr>
	<tr><th scope="row">Lotus Europa</th><td>30.4</td><td>4</td><td> 95.1</td><td>113</td><td>3.77</td><td>1.513</td><td>16.90</td><td>1</td><td>1</td><td>5</td><td>2</td></tr>
	<tr><th scope="row">Ford Pantera L</th><td>15.8</td><td>8</td><td>351.0</td><td>264</td><td>4.22</td><td>3.170</td><td>14.50</td><td>0</td><td>1</td><td>5</td><td>4</td></tr>
	<tr><th scope="row">Ferrari Dino</th><td>19.7</td><td>6</td><td>145.0</td><td>175</td><td>3.62</td><td>2.770</td><td>15.50</td><td>0</td><td>1</td><td>5</td><td>6</td></tr>
	<tr><th scope="row">Maserati Bora</th><td>15.0</td><td>8</td><td>301.0</td><td>335</td><td>3.54</td><td>3.570</td><td>14.60</td><td>0</td><td>1</td><td>5</td><td>8</td></tr>
	<tr><th scope="row">Volvo 142E</th><td>21.4</td><td>4</td><td>121.0</td><td>109</td><td>4.11</td><td>2.780</td><td>18.60</td><td>1</td><td>1</td><td>4</td><td>2</td></tr>
</tbody>
</table>
<table class="dataframe">
<caption>A data.frame: 16 × 11</caption>
<thead>
	<tr><th></th><th scope="col">mpg</th><th scope="col">cyl</th><th scope="col">disp</th><th scope="col">hp</th><th scope="col">drat</th><th scope="col">wt</th><th scope="col">qsec</th><th scope="col">vs</th><th scope="col">am</th><th scope="col">gear</th><th scope="col">carb</th></tr>
	<tr><th></th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope="row">Ferrari Dino</th><td>19.7</td><td>6</td><td>145.0</td><td>175</td><td>3.62</td><td>2.770</td><td>15.50</td><td>0</td><td>1</td><td>5</td><td>6</td></tr>
	<tr><th scope="row">Valiant</th><td>18.1</td><td>6</td><td>225.0</td><td>105</td><td>2.76</td><td>3.460</td><td>20.22</td><td>1</td><td>0</td><td>3</td><td>1</td></tr>
	<tr><th scope="row">Mazda RX4 Wag</th><td>21.0</td><td>6</td><td>160.0</td><td>110</td><td>3.90</td><td>2.875</td><td>17.02</td><td>0</td><td>1</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Merc 450SE</th><td>16.4</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>4.070</td><td>17.40</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Pontiac Firebird</th><td>19.2</td><td>8</td><td>400.0</td><td>175</td><td>3.08</td><td>3.845</td><td>17.05</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">Camaro Z28</th><td>13.3</td><td>8</td><td>350.0</td><td>245</td><td>3.73</td><td>3.840</td><td>15.41</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Porsche 914-2</th><td>26.0</td><td>4</td><td>120.3</td><td> 91</td><td>4.43</td><td>2.140</td><td>16.70</td><td>0</td><td>1</td><td>5</td><td>2</td></tr>
	<tr><th scope="row">Merc 450SLC</th><td>15.2</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>3.780</td><td>18.00</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Toyota Corona</th><td>21.5</td><td>4</td><td>120.1</td><td> 97</td><td>3.70</td><td>2.465</td><td>20.01</td><td>1</td><td>0</td><td>3</td><td>1</td></tr>
	<tr><th scope="row">Cadillac Fleetwood</th><td>10.4</td><td>8</td><td>472.0</td><td>205</td><td>2.93</td><td>5.250</td><td>17.98</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Duster 360</th><td>14.3</td><td>8</td><td>360.0</td><td>245</td><td>3.21</td><td>3.570</td><td>15.84</td><td>0</td><td>0</td><td>3</td><td>4</td></tr>
	<tr><th scope="row">Merc 450SL</th><td>17.3</td><td>8</td><td>275.8</td><td>180</td><td>3.07</td><td>3.730</td><td>17.60</td><td>0</td><td>0</td><td>3</td><td>3</td></tr>
	<tr><th scope="row">Merc 280</th><td>19.2</td><td>6</td><td>167.6</td><td>123</td><td>3.92</td><td>3.440</td><td>18.30</td><td>1</td><td>0</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">AMC Javelin</th><td>15.2</td><td>8</td><td>304.0</td><td>150</td><td>3.15</td><td>3.435</td><td>17.30</td><td>0</td><td>0</td><td>3</td><td>2</td></tr>
	<tr><th scope="row">Merc 280C</th><td>17.8</td><td>6</td><td>167.6</td><td>123</td><td>3.92</td><td>3.440</td><td>18.90</td><td>1</td><td>0</td><td>4</td><td>4</td></tr>
	<tr><th scope="row">Fiat X1-9</th><td>27.3</td><td>4</td><td> 79.0</td><td> 66</td><td>4.08</td><td>1.935</td><td>18.90</td><td>1</td><td>1</td><td>4</td><td>1</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">nrow<span class="token punctuation">(</span>mtcars_sample<span class="token punctuation">)</span>
</code></pre>
<p>16</p>
<pre class=" language-r"><code class="prism  language-r">
bootstrap_samples <span class="token operator">&lt;-</span> rep_sample_n<span class="token punctuation">(</span>mtcars_sample<span class="token punctuation">,</span> size <span class="token operator">=</span> <span class="token number">16</span><span class="token punctuation">,</span> reps <span class="token operator">=</span> <span class="token number">1000</span><span class="token punctuation">,</span> replace <span class="token operator">=</span> <span class="token boolean">TRUE</span><span class="token punctuation">)</span>

bootstrap_sample_estimates <span class="token operator">&lt;-</span> bootstrap_samples <span class="token percent-operator operator">%&gt;%</span>
  group_by<span class="token punctuation">(</span>replicate<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span> <span class="token comment"># technically the data is already grouped, but i'm putting this here to be extra explicit</span>
  summarize<span class="token punctuation">(</span>avg_mpg <span class="token operator">=</span> mean<span class="token punctuation">(</span>mpg<span class="token punctuation">,</span> na.rm <span class="token operator">=</span> <span class="token boolean">TRUE</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
bootstrap_sample_estimates

</code></pre>
<table class="dataframe">
<caption>A tibble: 1000 × 2</caption>
<thead>
	<tr><th scope="col">replicate</th><th scope="col">avg_mpg</th></tr>
	<tr><th scope="col">&lt;int&gt;</th><th scope="col">&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td> 1</td><td>17.79375</td></tr>
	<tr><td> 2</td><td>18.99375</td></tr>
	<tr><td> 3</td><td>17.83750</td></tr>
	<tr><td> 4</td><td>19.40625</td></tr>
	<tr><td> 5</td><td>18.55625</td></tr>
	<tr><td> 6</td><td>18.55625</td></tr>
	<tr><td> 7</td><td>17.18750</td></tr>
	<tr><td> 8</td><td>18.95000</td></tr>
	<tr><td> 9</td><td>16.02500</td></tr>
	<tr><td>10</td><td>18.16875</td></tr>
	<tr><td>11</td><td>18.10625</td></tr>
	<tr><td>12</td><td>16.43125</td></tr>
	<tr><td>13</td><td>17.37500</td></tr>
	<tr><td>14</td><td>18.81875</td></tr>
	<tr><td>15</td><td>17.52500</td></tr>
	<tr><td>16</td><td>17.36250</td></tr>
	<tr><td>17</td><td>18.11875</td></tr>
	<tr><td>18</td><td>19.05000</td></tr>
	<tr><td>19</td><td>19.17500</td></tr>
	<tr><td>20</td><td>20.42500</td></tr>
	<tr><td>21</td><td>17.73125</td></tr>
	<tr><td>22</td><td>17.20000</td></tr>
	<tr><td>23</td><td>18.18125</td></tr>
	<tr><td>24</td><td>17.76250</td></tr>
	<tr><td>25</td><td>17.92500</td></tr>
	<tr><td>26</td><td>17.79375</td></tr>
	<tr><td>27</td><td>18.14375</td></tr>
	<tr><td>28</td><td>18.15000</td></tr>
	<tr><td>29</td><td>17.50625</td></tr>
	<tr><td>30</td><td>19.50000</td></tr>
	<tr><td>⋮</td><td>⋮</td></tr>
	<tr><td> 971</td><td>17.68125</td></tr>
	<tr><td> 972</td><td>18.31875</td></tr>
	<tr><td> 973</td><td>19.53125</td></tr>
	<tr><td> 974</td><td>17.24375</td></tr>
	<tr><td> 975</td><td>18.93750</td></tr>
	<tr><td> 976</td><td>17.95000</td></tr>
	<tr><td> 977</td><td>17.61250</td></tr>
	<tr><td> 978</td><td>17.95625</td></tr>
	<tr><td> 979</td><td>17.81250</td></tr>
	<tr><td> 980</td><td>16.95625</td></tr>
	<tr><td> 981</td><td>18.69375</td></tr>
	<tr><td> 982</td><td>21.27500</td></tr>
	<tr><td> 983</td><td>18.77500</td></tr>
	<tr><td> 984</td><td>19.20625</td></tr>
	<tr><td> 985</td><td>19.71250</td></tr>
	<tr><td> 986</td><td>19.81875</td></tr>
	<tr><td> 987</td><td>19.19375</td></tr>
	<tr><td> 988</td><td>18.50000</td></tr>
	<tr><td> 989</td><td>18.18750</td></tr>
	<tr><td> 990</td><td>17.76250</td></tr>
	<tr><td> 991</td><td>18.70000</td></tr>
	<tr><td> 992</td><td>18.90625</td></tr>
	<tr><td> 993</td><td>18.35625</td></tr>
	<tr><td> 994</td><td>18.04375</td></tr>
	<tr><td> 995</td><td>17.89375</td></tr>
	<tr><td> 996</td><td>18.21250</td></tr>
	<tr><td> 997</td><td>17.87500</td></tr>
	<tr><td> 998</td><td>18.38750</td></tr>
	<tr><td> 999</td><td>17.39375</td></tr>
	<tr><td>1000</td><td>19.02500</td></tr>
</tbody>
</table>
<pre class=" language-r"><code class="prism  language-r">ggplot<span class="token punctuation">(</span>bootstrap_sample_estimates<span class="token punctuation">,</span> aes<span class="token punctuation">(</span>x <span class="token operator">=</span> avg_mpg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span> geom_histogram<span class="token punctuation">(</span><span class="token punctuation">)</span>

bootstrap_sample_estimates <span class="token percent-operator operator">%&gt;%</span>
    pull<span class="token punctuation">(</span>avg_mpg<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
    mean<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<pre><code>[1m[22m`stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
</code></pre>
<p>18.237625</p>
<p><img src="output_62_2.svg" alt="svg"></p>
<pre class=" language-r"><code class="prism  language-r">mtcars <span class="token operator">|</span><span class="token operator">&gt;</span>
    pull<span class="token punctuation">(</span>mpg<span class="token punctuation">)</span> <span class="token operator">|</span><span class="token operator">&gt;</span>
    mean<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<p>20.090625</p>
<pre class=" language-r"><code class="prism  language-r">s_size <span class="token operator">&lt;-</span> <span class="token number">30</span>

mtcars_sample <span class="token operator">&lt;-</span> mtcars <span class="token operator">|</span><span class="token operator">&gt;</span> sample_n<span class="token punctuation">(</span>size <span class="token operator">=</span> s_size<span class="token punctuation">)</span>
bootstrap_samples <span class="token operator">&lt;-</span> rep_sample_n<span class="token punctuation">(</span>mtcars_sample<span class="token punctuation">,</span> size <span class="token operator">=</span> s_size<span class="token punctuation">,</span> reps <span class="token operator">=</span> <span class="token number">1000</span><span class="token punctuation">,</span> replace <span class="token operator">=</span> <span class="token boolean">TRUE</span><span class="token punctuation">)</span>

bootstrap_sample_estimates <span class="token operator">&lt;-</span> bootstrap_samples <span class="token percent-operator operator">%&gt;%</span>
  group_by<span class="token punctuation">(</span>replicate<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span> <span class="token comment"># technically the data is already grouped, but i'm putting this here to be extra explicit</span>
  summarize<span class="token punctuation">(</span>avg_mpg <span class="token operator">=</span> mean<span class="token punctuation">(</span>mpg<span class="token punctuation">,</span> na.rm <span class="token operator">=</span> <span class="token boolean">TRUE</span><span class="token punctuation">)</span><span class="token punctuation">)</span>

ggplot<span class="token punctuation">(</span>bootstrap_sample_estimates<span class="token punctuation">,</span> aes<span class="token punctuation">(</span>x <span class="token operator">=</span> avg_mpg<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">+</span> geom_histogram<span class="token punctuation">(</span><span class="token punctuation">)</span>

bootstrap_sample_estimates <span class="token percent-operator operator">%&gt;%</span>
    pull<span class="token punctuation">(</span>avg_mpg<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
    mean<span class="token punctuation">(</span><span class="token punctuation">)</span>

bootstrap_sample_estimates <span class="token percent-operator operator">%&gt;%</span>
    pull<span class="token punctuation">(</span>avg_mpg<span class="token punctuation">)</span> <span class="token percent-operator operator">%&gt;%</span>
    sd<span class="token punctuation">(</span><span class="token punctuation">)</span>
</code></pre>
<pre><code>[1m[22m`stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
</code></pre>
<p>19.8384866666667</p>
<p>1.01950872541472</p>
<p><img src="output_64_3.svg" alt="svg"></p>
<pre class=" language-r"><code class="prism  language-r">
</code></pre>
<p><a href="https://www.openai.com">chat</a><br>
<a href="http://datasciencebook.ca">doc</a></p>

