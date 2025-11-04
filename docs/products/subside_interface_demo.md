---
title: SUBSIDE Interface Portal
author: 
   - DSO team
   - TACC Development Team
created: 2025-10-31
hide: 
   - navigation
   - toc
---

# SUBSIDE - Subsidence System for Insight and Data Exploration

## Interactive Three-Tiered Interface

The SUBSIDE interface provides comprehensive access to Texas subsidence data through three distinct user modes, each tailored to specific stakeholder needs as identified in Task 1.4 of the TWDB-TACC collaboration.

<div class="interface-embed" style="width: 100%; margin: 20px 0;">
  <iframe 
    width="100%" 
    height="900" 
    frameBorder="0" 
    src="../../webpages/subside_interface/subside_interface.html" 
    title="SUBSIDE Interactive Interface">
  </iframe>
</div>

## Interface Modes

### 🏠 Public Access
Simple, intuitive tools for property owners and residents to:
- Check property-specific subsidence risk
- View visual subsidence indicators
- Access educational resources
- Download assessment reports

### 💼 Professional Dashboard
Advanced capabilities for water managers and infrastructure operators:
- GIS integration tools
- Scenario modeling capabilities
- Regional trend analysis
- Infrastructure risk mapping
- Custom reporting tools

### 🔬 Technical Portal
Full data access for researchers and developers:
- Raw GPS and InSAR datasets
- RESTful API endpoints
- Cloud computing resources via Jupyter
- Custom processing pipelines
- Comprehensive metadata access

## Data Sources

The system integrates multiple monitoring technologies:

| Data Type | Coverage | Update Frequency | Format |
|-----------|----------|-----------------|---------|
| **GPS Networks** | 847 stations | Real-time | RINEX, CSV |
| **InSAR (Sentinel-1)** | Statewide | 6-12 days | GeoTIFF, NetCDF |
| **Groundwater Monitoring** | 23 counties | Daily | JSON, CSV |
| **Extensometer Data** | Key locations | Continuous | Time-series |

## System Architecture

The SUBSIDE architecture implements:
- **Progressive disclosure** of complexity based on user expertise
- **OGC-compliant** web services for GIS integration
- **Cloud-native** design for scalability
- **FAIR data principles** for findability and reusability

## Quick Start Guide

### For Public Users
1. Click the **Public** mode button
2. Enter your property address in the search bar
3. Review your property's subsidence risk assessment
4. Download a report for your records

### For Professionals
1. Select **Professional** mode
2. Access the GIS integration tools
3. Upload your infrastructure data
4. Run scenario models for planning

### For Researchers
1. Choose **Technical** mode
2. Browse available datasets
3. Access API documentation
4. Set up cloud computing environment

## API Access

### REST Endpoints
```
GET /api/v1/gps/{station_id}/timeseries
GET /api/v1/insar/coverage/{bbox}
GET /api/v1/subsidence/rate/{lat}/{lon}
POST /api/v1/analysis/custom
```

### Authentication
```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
     https://subside.tacc.utexas.edu/api/v1/datasets
```

## Data Standards

All data follows established standards:
- **GPS**: IGS standards for RINEX format
- **InSAR**: CEOS SAR format specifications
- **Metadata**: ISO 19115 geographic information
- **Web Services**: OGC WMS/WFS compliance

## Support Resources

### Documentation
- [User Guide](./docs/user-guide.md)
- [API Reference](./docs/api-reference.md)
- [Data Dictionary](./docs/data-dictionary.md)
- [Processing Workflows](./docs/workflows.md)

### Training Materials
- [Video Tutorials](./tutorials/)
- [Jupyter Notebooks](./notebooks/)
- [Sample Datasets](./samples/)

### Contact Information
- **Technical Support**: subside-support@tacc.utexas.edu
- **Data Inquiries**: data@twdb.texas.gov
- **Partnership Requests**: partnerships@tacc.utexas.edu

## System Requirements

### Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### Recommended Specifications
- **Public Interface**: Any modern browser
- **Professional Dashboard**: 8GB RAM, stable internet
- **Technical Portal**: 16GB RAM, high-speed connection

## Data Attribution

When using SUBSIDE data, please cite:
```
Texas Water Development Board & Texas Advanced Computing Center (2025). 
SUBSIDE: Subsidence System for Insight and Data Exploration. 
Contract #2300012717. https://subside.tacc.utexas.edu
```

## Terms of Use

By accessing SUBSIDE, users agree to:
- Appropriate use of computational resources
- Proper data attribution in publications
- No upload of personally identifiable information
- Compliance with TACC acceptable use policies

## Updates & Releases

### Current Version: 1.0.0 (October 2025)
- Initial three-tiered interface launch
- Houston-Galveston pilot region
- Core data integration complete

### Upcoming Features (v1.1.0)
- Statewide coverage expansion
- Machine learning predictions
- Mobile application
- Advanced visualization tools

## Related Resources

- [Texas Subsidence Maps](./texas_subsidence_resources.md)
- [Groundwater Management Areas](./groundwater_management.md)
- [Infrastructure Risk Assessment](./infrastructure_risk.md)
- [Educational Materials](./education/)

---

*Last Updated: October 31, 2025*  
*Contract: #2300012717*  
*Partners: TWDB | UT Austin | TACC*