Norwegian Government Domains
=========================

An incomplete listing of Norwegian government domains.

You can **download the list [as a .csv file](https://github.com/byeskille/norway-gov-domains/blob/master/data/domains.csv)**.

We try to use the same format as the [US GSA](https://github.com/GSA/data) ([example](https://github.com/GSA/data/blob/e0de99db0e1367e304043e88dbd4da8f391774be/dotgov-domains/2016-01-19-full.csv)), so the CSV file has a header of `Domain name,Domain type,Agency,City,State,Local municipality,Country,ORGNR,Sektorkode` and currently contains domains registered under the .no TLD by local, regional and central government agencies + all domains from category domains .kommune.no/.herad.no (local government) and .dep.no/.stat.no (central government) + some .mil.no subdomains.

## Variants

If you only want a subset of the available data, variants filtered by `Source` are provided:

* [`data/domains.csv`](data/domains.csv) contains everything
* [`data/domains.federal.csv`](data/domains.federal.csv) contains only central government agencies (`Federal Agency`) based on category domain lists and Central Coordinating Register for Legal Entities.
* [`data/domains.local.csv`](data/domains.local.csv) contains only domains related to regional and local government based on category domain lists and Central Coordinating Register for Legal Entities.

## Why?

There currently isn't a publicly available directory of all the domain names registered by the Norwegian government and its agencies. Such a directory would be useful for people looking to get an aggregate view of government websites and how they are hosted. For example, [Ben Balter](http://ben.balter.com) has been doing some great work [analyzing](http://ben.balter.com/2015/05/11/third-analysis-of-federal-executive-dotgovs/) the [official set of US `.gov` domains](https://github.com/GSA/data/tree/gh-pages/dotgov-domains).

This is by no means an official or a complete list. It is intended to be a first step toward a better understanding of how the government is managing its official sites.

The list was made in order to do journalistic reporting by the Norwegian Broadcasting Corp. (NRK) into HTTPS usage on government sites.

See news stories:

* [http://www.nrk.no/dokumentar/xl/1.12854582](http://www.nrk.no/dokumentar/xl/1.12854582)
* [http://www.nrk.no/dokumentar/xl/1.12859753](http://www.nrk.no/dokumentar/xl/1.12859753)

## What can I do with it?

* Plug the CSV into [18F/domain-scan](https://github.com/18F/domain-scan) to get more data (like HTTPS support) about the domains
* Use it a basis for more simple testing with the [SSL Labs API](https://github.com/ssllabs/ssllabs-scan/blob/stable/ssllabs-api-docs.md) and [`ssllabs-scan](https://github.com/ssllabs/ssllabs-scan)
* Check the IPv6 reachability
* Test if the sites are reachable even without the `www.` subdomain
* ...?




## Sources

* `data/source/kommune-herad-ks.csv`: list from [association for local governments KS](http://www.ks.no/fagomrader/om-ks/Kommunikasjon/kommune.no/) containing all category domains under .kommune.no + .herad.no, aquired with a freedom of information request
* `data/source/dep_stat_no_24112015.pdf`: list from [shared services agency DSS](https://dss.dep.no/english) containing all category domains under .dep.no + .stat.no , aquired with a freedom of information request
* `data/source/gov-no-norid.csv`: list from Norwegian domain registry Norid, aquired by asking for a database query into the whois database for domains owned by government entities [`data/source/brreg-list.csv`](data/source/brreg-list.csv)
* `data/source/brreg-list.csv`: list of government entities from Central Coordinating Register for Legal Entities at Brønnøysund Register, aquired from [open data](http://data.brreg.no/oppslag/enhetsregisteret/enheter.xhtml) and collected with filter on sector code `sektorkode`: `6100 – Stats- og trygdeforvaltning, 6500 – Kommuneforvaltningen, 1100 – Statens forretningsdrift, 3900 – Statlige låneinstitutter mv.`
* `data/source/mil_no_domains.csv`: manually curated list of domains under the Norwegian category domain .mil.no based on Google searches

## Contributing

This is in no way an official list, but was used for a journalistic project. If we do follow ups a more comprihensive list would of course be could. So do give input! Please feel free to [create an issue](https://github.com/byeskille/norway-gov-domains/issues) or [submit a pull request](https://github.com/byeskille/norway-gov-domains/pulls) if you notice something that can be better. Specifically, suggesting additional pages we can look into and domains that are either not found or have incorrect organization names associated with them would be very helpful.

## Ideas

* set up a system to track the HTTPS usage ala [`pulse`](https://github.com/18F/pulse)
  * include doing the tests with the full [`domain-scan`](https://github.com/18F/domain-scan) and not just [`ssllabs-scan`](https://github.com/ssllabs/ssllabs-scan)
* get a better domain list
  * try to get a more official list of domains with a freedom of information request


## Thanks

Thanks to [@esonderegger](https://github.com/esonderegger) for the [dotmil domains project](https://github.com/esonderegger/dotmil-domains) and [@robbi5](https://github.com/robbi5/) for the [German Government Domains](https://github.com/robbi5/german-gov-domains/) that served as a template for this repo.