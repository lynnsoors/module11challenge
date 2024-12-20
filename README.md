<h3>Background</h3>
<p>You’re now ready to take on a full web-scraping and data analysis project. You’ve learned to identify HTML elements on a page, identify their <code>id</code> and <code>class</code> attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.</p>
<p>As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating your insights.</p>
<h3>What You're Creating</h3>
<p>This new assignment consists of two technical products. You will submit the following deliverables:</p>
<ul>
<li>
<p>Deliverable 1: Scrape titles and preview text from Mars news articles.</p>
</li>
<li>
<p>Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.</p>
</li>
</ul>
<h3>Instructions</h3>
<h4>Part 1: Scrape Titles and Preview Text from Mars News</h4>
<p>Open the Jupyter Notebook in the starter code folder named <code>part_1_mars_news.ipynb</code>. You will work in this code as you follow the steps below to scrape the Mars News website.</p>
<ol>
<li>
<p>Use automated browsing to visit the <a href="https://static.bc-edx.com/data/web/mars_news/index.html">Mars news site</a>. Inspect the page to identify which elements to scrape.</p>
<blockquote class="callout hint">
<strong>hint</strong>
<p>To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools.</p>
</blockquote>
</li>
<li>
<p>Create a Beautiful Soup object and use it to extract text elements from the website.</p>
</li>
<li>
<p>Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:</p>
<ul>
<li>
<p>Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: <code>title</code> and <code>preview</code>. An example is the following:</p>
<pre><code class="language-python">{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
</code></pre>
</li>
<li>
<p>Store all the dictionaries in a Python list.</p>
</li>
<li>
<p>Print the list in your notebook.</p>
</li>
</ul>
</li>
<li>
<p>Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)</p>
</li>
</ol>
<h4>Part 2: Scrape and Analyze Mars Weather Data</h4>
<p>Open the Jupyter Notebook in the starter code folder named <code>part_2_mars_weather.ipynb</code>. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.</p>
<ol>
<li>
<p>Use automated browsing to visit the <a href="https://static.bc-edx.com/data/web/mars_facts/temperature.html">Mars Temperature Data Site</a>. Inspect the page to identify which elements to scrape. Note that the URL is <code>https://static.bc-edx.com/data/web/mars_facts/temperature.html</code>.</p>
<blockquote class="callout hint">
<strong>hint</strong>
<p>To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools to discover whether the table contains usable classes.</p>
</blockquote>
</li>
<li>
<p>Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas <code>read_html</code> function. However, use Beautiful Soup here to continue sharpening your web scraping skills.</p>
</li>
<li>
<p>Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:</p>
<ul>
<li>
<code>id</code>: the identification number of a single transmission from the Curiosity rover</li>
<li>
<code>terrestrial_date</code>: the date on Earth</li>
<li>
<code>sol</code>: the number of elapsed sols (Martian days) since Curiosity landed on Mars</li>
<li>
<code>ls</code>: the solar longitude</li>
<li>
<code>month</code>: the Martian month</li>
<li>
<code>min_temp</code>: the minimum temperature, in Celsius, of a single Martian day (sol)</li>
<li>
<code>pressure</code>: The atmospheric pressure at Curiosity's location</li>
</ul>
</li>
<li>
<p>Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate <code>datetime</code>, <code>int</code>, or <code>float</code> data types.</p>
<blockquote class="callout hint">
<strong>hint</strong>
<p>You can use the Pandas <code>astype</code> and <code>to_datetime</code> methods to accomplish this task.</p>
</blockquote>
</li>
<li>
<p>Analyze your dataset by using Pandas functions to answer the following questions:</p>
<ul>
<li>How many months exist on Mars?</li>
<li>How many Martian (and not Earth) days worth of data exist in the scraped dataset?</li>
<li>What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
<ul>
<li>Find the average minimum daily temperature for all of the months.</li>
<li>Plot the results as a bar chart.</li>
</ul>
</li>
<li>Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
<ul>
<li>Find the average daily atmospheric pressure of all the months.</li>
<li>Plot the results as a bar chart.</li>
</ul>
</li>
<li>About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
<ul>
<li>Consider how many days elapse on Earth in the time that Mars circles the Sun once.</li>
<li>Visually estimate the result by plotting the daily minimum temperature.</li>
</ul>
</li>
</ul>
</li>
<li>
<p>Export the DataFrame to a CSV file.</p>
