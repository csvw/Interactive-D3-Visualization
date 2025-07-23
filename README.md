# Interactive D3 Visualization
Data visualization for topic modeling of freeCodeCamp's chat log dataset.

## Problem Description

Students formed teams and were tasked with selecting and analyzing a large dataset (preferably several GB or larger). They were then required to develop an interactive visualization that allowed users to explore the results of the analysis. Over the course of the semester, students were exposed to a wide variety of analytic and visualazation tools, such as D3, Tableau, Hadoop, AWS, and Microsoft Azure. Teams were allowed to utilize any tools and data that they saw fit, provided that they met the requirements outlined above.

My team was interested in exploring natural language processing. After settling on the Gitter chat logs for our data set, we decided to utilize a technique called Latent Dirichlet Allocation. LDA can be used to perform topic modeling on textual corpora. Topic modeling clusters documents into related groups. LDA in particular relates documents to each other by identifying words that frequently co-occur across multiple documents.

We were interested in applying topic modeling to the Gitter chat logs to identify popular trends. Our goal was to classify all the chat messages according to their subject and then display the popularity of those subjects over time.

## D3 Visualization

My primary responsibility was to develop the visualization that would enable users to explore the results of our analysis. I built the visualization using JavaScript, HTML, CSS and D3. A screenshot of the visualization is shown below:

![alt text]([https://github.com/csvw/Interactive-D3-Visualization/blob/master/Screenshot-D3.png](https://raw.githubusercontent.com/csvw/Interactive-D3-Visualization/refs/heads/master/Screenshot-D3.png))

Each trend line corresponds to a particular topic. The large green trend line, for example, relates primarily to debugging. Each bubble corresponds to the popularity of that topic during a particular time slice: the width reveals the number of messages associated with that topic, and the height reveals the number of users participating in that topic.

The charts on the left and right are complementary--the chart on the left shows the relative popularity of different topics over time, while the chart on the right provides a more concise view of a particular topic's popularity during any given month.

The visualization is interactive. Users can hide or reveal diffent trend lines by clicking on the colored boxes on the left hand side of the screen. Hoving the mouse over those boxes reveals the most popular words associated with that topic, and hovering over any of the bubbles displays statistics about the activity of that topic during the month associated with that bubble.

Users can change the granularity of the trend lines, grouping messages by weeks or months. Additionally, the trend lines can be animated by using the buttons on the bottom right, revealing the relative growth rates of the topics.

Finally, the chart on the left can be scrolled, zoomed, and resized, allowing users to investigate the trend lines at different scales.

## Running the Program

If you want to run the visualization, then you will need to start a localhost server and navigate to the directory containing visualization.html. Opening visualization.html from localhost will start the visualization.

To start a simple server, you will need to install python.

Instructions for installing python3 can be found here:
https://docs.python-guide.org/starting/install3/linux/
https://realpython.com/installing-python/

On Linux, a webserver can be started (after installing python) by running the following in the terminal:

python -m http.server

If you have python2 installed, then you can instead run:

python -m SimpleHTTPServer

Then type localhost:8000 into your web browser. From there, you can navigate to the directory containing visualization.html.

Instructions for starting a local server on Windows are similar, and will still require the installation of python. Instructions can be found here:

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/set_up_a_local_testing_server

