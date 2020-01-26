# info202project

This project served to highlight the size and scope of multinational companies located in the US.

![alt-text](http://www.convergencealimentaire.info/map.jpg)

By law, public companies are required to submit financial information, including annual 10-K financial reports, to the US Security and Exchange Commission. Within these annual reports, companies will provide an Exhibit-21 document listing the subsidiaries they own. 

In starting this project, we used the Edgar package (https://pypi.org/project/edgar/) to develop a program that would automatically pull and classify Companies and their subsidiaries. Following initial development, we opted to instead use the dataset provided by Corpwatch API (http://api.corpwatch.org/) a non-profit organization that had pulled and classifed companies in the SEC. Seeing as how Corpwatch utilized the same strategy of pulling 10-K and EX-21 documents to highlight parent-child relationships, we felt confident in our instincts for tackling this problem.

Using Corpwatch datasets, we created a master dataset allowing us to query information on names, locations, and industries. Using a command line interface, users can query specific companies or industies. 
- When querying by company, the program will display any companies related to it (either parent or children). For multinational companies, the program would also generate a report that would show all subsidiaries, locations, and industries associated with that company. 
- When querying by industry, the program will identify multinational companies that owned subsidiaries in the selected industry. Using Pandas, we would then generate a list of the top 25 multinationals in that field based on number of subsidiaries owned, usually identifying unexpected relationships or stakes. 
