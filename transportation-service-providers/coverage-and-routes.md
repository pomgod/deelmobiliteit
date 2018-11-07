# Coverage and Routes

Mobility as a Service \(MaaS\) operators need to plan journies on behalf of passengers. In order to help people get where they want to go, it is useful to know what transportation options are available between the passenger origin and destination.

## Coverage

Coverage describes the area and times in which a Transportation Service Provider \(TSP\) operates. The area will typically be in the form of a geographic polygon, indicating the extents of the service area. It is also important to know what times of day people may access the TSP vehicles, as people may travel through a coverage area at all hours.

## Routes and Stops

Some TSPs operate vehicles with fixed routes, such as bus or tram lines. Generally, routes consist of lines that connect points, such as bus lines with stops. However, some transportation options consist mainly of points, such as bike share docks, or car share free-floating zones.

Regardless of the underlying geometry, it is important to publish route information in common formats, so that MaaS operators can help passengers find routes through one or more TSP network\(s\).

## Coverage and routes actions

When designing a **Coverage API**, some or all of the following may be important to MaaS Providers:

* _get_ coverage 
  * area - get a \(multi\) polygon describing the entire coverage area
  * points - get points that are part of the service offering \(e.g. charging stations, bus stops, etc\)
    * within - get points within a provided geometry
    * near - get points within a given radius of given geographic coordinate
* _get_ within coverage area - determine whether a geographic point is within coverage area

## Further reading

* [General Transit Feed Specification](https://en.wikipedia.org/wiki/General_Transit_Feed_Specification) - defines a common format for [public transportation schedules](https://en.wikipedia.org/wiki/Public_transport_timetable) and associated geographic information.
* [NeTEx](https://en.wikipedia.org/wiki/NeTEx) - Technical standard for exchanging Public Transport Information as XML documents.
* [Service Interface for Real Time Information](https://en.wikipedia.org/wiki/Service_Interface_for_Real_Time_Information) - allows distributed computers to exchange real-time information about [public transport](https://en.wikipedia.org/wiki/Public_transport) services and vehicles.

