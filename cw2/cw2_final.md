# Data Biography

## Student Number: 20170567



### 1. Who collected the data?

Murray Cox founded Inside Airbnb and had support from Tom Slee on the data collection and report. Cox maintains Inside Airbnb on an ongoing basis.

---

### 2. Why did they collect it?

Cox and Slee, initially collecting data independent of another, were collecting for similar reasons. They believed that Airbnb was negatively affecting the communities in which it operated and in many jurisdictions, like NYC, were breaking local housing laws [1]. They wanted to be able to showcase this through their data.

---

### 3. How was it collected?

Cox and Slee have stated that the data “was assembled by programmatically compiling public information from Airbnb’s website” [2]. The technologies used are D3, Crossfilter, dc.js, Leaflet, Bootstrap, jQuery, Select2, Python, PostgreSQL and Google Fonts. [3]

Based on Slee’s website and the acknowledgement on Inside Airbnb, it appears that Python does the heavy lifting for the data collection. The Python code scrapes through the website pulling information deemed useful by the authors.

---

### 4. What useful information does it contain?

The data collected contains 74 columns with properties listed by a unique identifier (id) in the first column - the subsequent 73 columns contain observations regarding the property listed in the first column.

Column information ranges from text descriptions of the property and neighbourhood, URLs for the property and hosts to the latitude and longitude of the property.

Depending on subsequent research, data could potentially be grouped into the following categories:

* Location - the physical location of the property (e.g. neighbourhood)
* Property - details of the property itself (e.g. price)
* Host - details on the host (e.g. host id)

---

### 5. What useful information is it missing?

Overall the data is missing qualitative information that backs up the validity and context of the scraped information. Do location coordinates match the neighbourhood listed by the host? Has this property been taken off in the past for breaking the rules?

---

### 6. To what extent is the data ‘complete’?

The data used by Inside Airbnb will never be truly complete as it is always taken at a point in time. Inevitably there will be changes between when it was scraped and subsequently analysed. Technology also limits completeness, as stated by Cox and Slee in the paper that listings that do not receive guests may not show up and other listings that are difficult to view may not appear as well. Based on the paper, they believe that their data represents approximately 95% of all active listings in a city. [2].

Though the data does provide a strong basis for the analysis of the Airbnb presence in a city or neighbourhood, it will always lack more comprehensive contextual information about the cities in which it operates. Information about an NYC neighbourhood will be significant to someone like Cox, a New Yorker, but nuance would be lost to a Londoner.

---

### 7. What kinds of analysis would this support?

Inside Airbnb say themselves that this data best answers questions like, "How many listings are in my neighbourhood and where are they?" or "Which hosts are running a business with multiple listings and where they? [2]. Speaking more generally than the Inside Airbnb examples, the data provides the ability to identify trends or patterns of the Airbnb presence, at the time it was taken from publicly available information on their website, in a city or community.

Trends that could be identified across sections of the data include price variance across a city, the frequency of properties across varying locations, or the variance of entire home properties or private rooms across neighbourhoods.

Textual analysis of the listings could also provide insight into how properties are being described across cities and neighbourhoods. A combination of textual analysis and a price analysis could provide insight on if language reflects the chosen price points.

---

### 8. What kinds of analysis would it *not* support?

In isolation, this data would not support analysis on the effect that Airbnb is having on the communities in which it operates. This data would not be able to analyse something like the effect of a widening rent gap in a community. A widening rent gap occurs when actual rents, current tenant rents (unknown in the Inside Airbnb data), begin to diverge from more significant Airbnb returns [4]. As this change occurs, it could not be analysed using only this data as the before and after Airbnb demography of a neighbourhood is unknown, especially around the makeup of permanent residents.

---

### 9. Which of the uses listed in #7 are ethical?

On their own, I believe that all uses listed in #7 are inherently ethical. The information scraped from the Airbnb website is added to the site willingly by individuals or parties who have chosen to become potential hosts. Analysing for things like pricing trends or the listings in a neighbourhood is not unethical on its own.

Issues around ethics arise when combined with the intent of analysis. Using the example of price analysis in #7, is it ethical for a property developer to attempt to identify neighbourhoods where there is a high rent gap in order to maximise their return on investment? A high percentage of people would consider this prudent due diligence and savvy business practice. It would also be a completely legal action to take in a market like London or New York City. Inevitably, however, it would be mean that long term residents, if they could not afford to say no to an offer, could not afford rent increases or had their landlords force them out, would be displaced. Is this result ethical? The question around ethics is ultimately is up to the individual, a jurisdiction can make laws to protect their constituents, but there will always be questionable things occurring on the fringes especially when large sums of money are at stake.

Like a hammer, knife or a gun, data analysis is a tool to reach a specific end. The rent gap analysis mentioned above could easily be flipped on its head to allow a city government to protect an at-risk community from potentially predatory investment. In the end, it comes down to a researcher’s ethics and motivations, but Joni Seager said it better than I could, “What gets counted, counts.” [5] Ethics will inevitably fray when real people turn into only numbers on a page.

Word Count 1,047

---

# References

[1]		M. Katz. (2017, Oct. 2). A Lone Data Whiz Is Fighting Airbnb — and Winning [Online]. Available: 		https://www.wired.com/2017/02/a-lone-data-whiz-is-fighting-airbnb-and-winning/

[2]		M. Cox and T. Slee, “How Airbnb’s data hid the facts in New York City”, Report [Online], February 10, 		2016. Available: http://insideairbnb.com/reports/how-airbnbs-data-hid-the-facts-in-new-york-city.pdf

[3]		Inside Airbnb. Behind Inside Airbnb [Online]. Available: http://insideairbnb.com/behind.html

[4]		A. Weisler and D. Wachsmuth. “Airbnb and the rent gap: Gentrification through the sharing 		economy,” Environment and Planning A: Economy and Space, vol. 50, iss. 6, pp. 1147-1170, 2018.

[5]		C. D’Ignazio and L. Klein. (2018) “Chapter Three: “What Gets Counted Counts,” in Data Feminism 		[Online]. Available: https://mitpressonpubpub.mitpress.mit.edu/pub/rykaknh1/release/4
