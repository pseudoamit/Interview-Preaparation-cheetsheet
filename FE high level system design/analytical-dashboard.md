# 1. Analytical Dashboard with One Million Records

Design a **high-performance analytical dashboard** that processes and visualizes **1 million records**.

## Requirements

An API returns **1,000,000 records in a single response**.

The frontend must:

1. Display the records in a **tabular format**.
2. Generate **20 analytical charts/graphs** based on the data.
3. Perform **all data processing on the frontend**.
4. Ensure the system remains **highly performant and responsive**.

## Constraints

- **Pagination is NOT allowed.**
- **Backend modifications are NOT allowed.**
- All **data transformations must happen on the frontend.**
- The UI must remain **smooth and responsive even with large datasets**.

## System Design Considerations

### Data Processing Strategy

How would you:

- Process **1 million records efficiently on the frontend**?
- Avoid **blocking the main thread**?
- Perform **data aggregation for charts**?

### Rendering Strategy

How would you render:

- Large **tables efficiently**?
- Multiple **charts derived from large datasets**?

Consider techniques such as:

- Virtualization
- Windowing
- Incremental rendering

### Performance Optimization

How would you optimize:

- Memory usage
- CPU usage
- Rendering performance
- Data transformations

### Parallel Processing

Would you use:

- **Web Workers**
- **Worker Threads**
- **Chunked data processing**

Explain how.

### Chart Rendering Strategy

How would you efficiently render **20 charts** derived from the dataset?

Consider:

- Memoization
- Lazy rendering
- Background computation

### Data Caching

Would you cache processed data?

If yes:

- Where would you cache it?
- How would you manage cache invalidation?

### Scalability

If the dataset grows to **10 million records**, how would your design change?
