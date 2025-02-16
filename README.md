# 🌍 GNNExplainer for Urban Planning and Environment Analysis

This project explores the application of **Graph Neural Networks (GNNs)** in urban planning and environmental studies, using **GNNExplainer** to interpret the influence of urban factors on city characteristics. GNNExplainer helps unveil insights into which variables, such as population density, accessibility to transportation, and environmental quality, contribute most to urban development patterns and health outcomes.

## 🌐 Applications

This project’s insights can significantly contribute to real-world urban planning, environmental policy-making, and public infrastructure management. Some concrete applications include:

- **Urban Zoning and Development**: By identifying the most influential factors impacting urban areas, such as housing prices, population density, and accessibility to green spaces, city planners can make informed decisions about zoning policies and development priorities. For example, areas with high population density but limited green spaces may be prioritized for park development to improve residents' quality of life.

- **Environmental Health Assessment**: The model's ability to weigh environmental factors like PM2.5 and CO levels helps policymakers understand how air quality correlates with public health. This understanding can guide regulations to improve air quality in regions with poor environmental conditions, particularly around high-traffic areas or industrial zones.

- **Transportation Planning**: GNNExplainer can identify how accessibility to public transportation—such as proximity to metro and bus stations—affects urban functionality and property values. By understanding these relationships, transit authorities can better allocate resources, such as increasing transportation routes in areas with poor accessibility but high demand for public transit.

- **Resource Allocation for Health and Education Facilities**: By analyzing the spatial distribution of educational and medical facilities in relation to population demographics, planners can identify underserved areas and prioritize them for new facility development. This ensures equitable access to essential services, especially in rapidly urbanizing regions.

- **Climate Resilience and Green Space Optimization**: Urban environments face challenges related to climate change, including extreme weather and pollution. By understanding how factors like the green view index (GREN) and walkability index (WAL) impact resident satisfaction and urban livability, city planners can incorporate green infrastructure into urban design to enhance resilience against climate-related impacts.

These applications illustrate how the model’s outputs can be directly leveraged to make cities more livable, equitable, and sustainable.

## Project Overview
This project is designed to implement and explain the decisions made by Graph Neural Networks (GNN) using the GNNExplainer tool. It consists of input and output data handling, as well as the core functionality script that facilitates model explanation.

## Folder Structure

### :open_file_folder: input file
- **Description**: Contains the input data files used by the GNN model.
- **Contents**: Data files (adjust this according to what actually is in the folder).

### :file_folder: output file
- **Description**: Stores the output from the GNN model, including predictions and model explanations.
- **Contents**: Result files (adjust this according to what actually is in the folder).

### :page_facing_up: GNNExplainer.py
- **Description**: Python script containing the implementation of the GNN model and the GNNExplainer functionality.
- **Usage**:
  ```bash
  python GNNExplainer.py [arguments]


## 🧠 Model Details

This GNN model is built using a **hybrid architecture** that combines **GraphSAGE** and **GAT (Graph Attention Network)** layers. The model can effectively capture complex spatial and non-spatial relationships among urban features, trained on data that includes factors like housing prices, distances to transportation hubs, air quality, and more.

### HybridModel Architecture
The model consists of:
- **GraphSAGE** layers for general neighborhood aggregation.
- **GAT** layers with multiple heads to apply attention to neighborhood nodes, enhancing the ability to identify influential relationships.
- **Dropout layers** for regularization, and a **final classification layer** for predictive tasks.

## 🔍 Explanation Workflow

The process of using **GNNExplainer** for feature and edge importance includes the following steps:
1. **Data Preparation**: Load node features, edge lists, and labels. Normalize the features for training and evaluation.
2. **Model Loading**: Load the pre-trained hybrid GNN model.
3. **Feature and Edge Importance Calculation**: Use GNNExplainer to assess the importance of features and edges for each node.
4. **Output Storage**: Save the resulting node and edge importance scores in CSV files.

## 📊 Input Data

This GNN model uses urban environment data with features such as:
- `HOP`: Housing prices (Yuan/m²)
- `POD`: Population density (people/m²)
- `DIS_BUS`: Distance to the nearest bus station (m)
- `POI_COM`: Number of commercial points of interest
- `PM2_5`: PM2.5 air pollution level (μg/m³ per day)
- ... and more environmental and socio-economic indicators.

Edges represent spatial or functional proximity between locations, providing the GNN model with critical relational information.

## 🚀 Getting Started

### Prerequisites

Ensure you have the following specific versions of libraries installed for proper compatibility:

- PyTorch (CPU version): `2.4.1`
- torch_geometric: `2.0.4`
- torch_scatter: `2.0.9`
- torch_sparse: `0.6.12`
- torch_cluster: `1.5.9`
- torch_spline_conv: `1.2.1`
- scikit-learn: `0.24.2`
- pandas: `1.3.3`
- numpy: `1.21.2`

To install all dependencies with the specified versions, use the following command:

```bash
pip install torch==2.4.1 torch_geometric==2.0.4 torch_scatter==2.0.9 \
torch_sparse==0.6.12 torch_cluster==1.5.9 torch_spline_conv==1.2.1 \
scikit-learn==0.24.2 pandas==1.3.3 numpy==1.21.2




