# LABORATORY 7: PostGIS to REST API to GIS Clients
---
## Description
This laboratory demonstrates how PostGIS, Flask REST API, and QGIS work together in a spatial data pipeline. It focuses on retrieving spatial data from PostGIS and serving it as GeoJSON for GIS clients.
---
## Dependencies
- Python 3.14
- Visual Studio Code
- flask
- flask-cors
- psycopg2-binary
- python-dotenv
---
## REFLECTION
---
### 1. What role does PostGIS play in this architecture?
- In the architecture of this laboratory, the PostGIS serves as the spatial database management system. It stores the parcel and road spatial features along with their related attribute data in a shared spatial database. It acts as the main source of spatial data that is accessed and published through the Flask API.
---
### 2. What role does Flask play in this laboratory?
- In this laboratory, the Flask serves as the REST API framework used to connect the spatial database and the GIS client. It retrieves spatial records from PostGIS, processes the data, and returns it as GeoJSON through API endpoints. The Flask acts as the connection between the database and GIS clients, allowing QGIS and other applications to access the spatial data through HTTP requests.
---
### 3. Why is GeoJSON useful for spatial web services?
- GeoJSON is useful for spatial web services because it provides a simple and common format for sharing spatial data through web services. It stores both geometry and attribute information in a format that is easy for applications and softwares to read. GeoJSON is also widely supported by GIS platforms, web maps, and APIs, making data sharing easier and compatible across different systems.
---
### 4. How does ST_AsGeoJSON() support distributed GIS?
- ST_AsGeoJSON() supports distributed GIS by converting PostGIS geometries into GeoJSON format that can be shared through web services and APIs. This allows spatial data stored in the database to be accessed by distributed GIS clients such as QGIS and web applications. It supports compatibility between systems by allowing different applications to access and interpret the same spatial information consistently.
---
### 5. Why is QGIS considered a heavy client?
- QGIS is considered a heavy client because it performs most of its visualization and processing tasks on the user’s computer instead of relying heavily on the server. It can render layers, analyze spatial data, edit geometries, and manage attributes locally using built-in GIS tools. QGIS also supports advanced plugins, spatial analysis functions, map layouts, and data editing tools that require strong local processing capabilities. Because of these features, QGIS can handle complex GIS operations and large spatial datasets directly on the client side.
---
### 6. Why is a REST API better than manually exporting shapefiles?
- A REST API is better than manually exporting shapefiles because it allows users and GIS clients to access updated spatial data directly from the database without repeatedly exporting files manually. Unlike manual shapefile exports, the data can be accessed in real time and changes in the database can immediately appear in connected GIS applications. REST APIs also help reduce file duplication, improve data sharing, and support flexible workflows where multiple users and systems can access the same spatial services simultaneously. This makes spatial data management faster, more consistent, and more efficient compared to manually transferring shapefiles between users and applications.
---
### 7. How does this laboratory demonstrate distributed geospatial computing?
- This laboratory demonstrates distributed geospatial computing by separating the system into independent components that communicate through web technologies. PostGIS stores the spatial data, Flask provides the API service, and QGIS accesses the spatial data as a client application. The workflow shows how spatial information can be distributed, accessed, and visualized across different systems using GeoJSON and REST services. It also demonstrates how spatial databases, web APIs, and GIS clients can work together to support real-time data sharing and distributed GIS workflows.
---
### 8. What advantages does service-based GIS architecture provide?
- The advantages of service-based GIS architecture are that it allows spatial data and GIS services to be shared more easily across multiple systems and users. It improves accessibility because clients can access spatial data remotely without needing direct database access or repeated file transfers. It also supports easier maintenance, better data management, and improved compatibility between different GIS platforms and applications. Another advantage is that updates made in the database can immediately be reflected in connected GIS clients and web services.
---
### 9. How does this architecture support scalability in spatial systems?
- This architecture supports scalability because additional users, applications, and GIS clients can connect to the same API and database services without changing the overall system design. The separation of the database, API, and client components allows each part of the system to be upgraded or expanded independently. It also makes system maintenance easier because updates and improvements can be applied to one component without affecting the entire workflow. The architecture can support larger spatial datasets, increased user demand, and additional GIS services as the system grows. It provides a foundation for future integration.
---
### Author
- Audrey Marie Justine A. Reyes
- MS Geomatics Engineering (GeoInf)