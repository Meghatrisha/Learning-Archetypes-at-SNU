# Learning-Archetypes-at-SNU

#### **Introduction:**

At Sister Nivedita University (SNU), faculty members have observed a wide spectrum of learning preferences among students. Some excel by meticulously studying books, others by consuming information through visual media like series, and some learn best through hands-on coding. To address this diversity and enhance educational outcomes, the university is launching a data-driven initiative to develop personalized mentoring strategies. This project, titled "The SNU Student Learning Archetypes Project," leverages unsupervised machine learning to group students into distinct learning profiles.

#### **Project Goal:**

The primary objective is to identify and define clear "learning archetypes" within the student body. By analyzing behavioral data, we aim to uncover patterns that differentiate students into groups such as "Bookworms," "Binge-Learners," and "Hybrid Learners." The insights gained will directly inform and enable the design of adaptive teaching and mentoring approaches.

#### **Core Data & Features:**

To achieve this, we will use a dataset that captures key student learning behaviors. The following features will be central to our analysis:

* **`books_read_past_year`**: A numerical feature representing the total number of books a student has read.
* **`reads_books`**: A binary feature indicating whether a student is a regular book reader.
* **`book_genre_top1`**: A categorical feature identifying the student's most-read book genre (e.g., academic, fiction, non-fiction).
* **`screen_time_movies_series_hours_per_week`**: A numerical feature measuring the weekly hours spent watching movies and series.
* **`binge_freq_per_week`**: A numerical feature quantifying the average number of times a student "binges" a series in a given week.

#### **Methodology:**

The project will follow a structured data science pipeline:

1.  **Data Preprocessing and Feature Engineering:** We will begin with a thorough cleaning of the raw data. This will include handling missing values and outliers. To create more meaningful insights, we will engineer new features, such as a "reading-to-screen ratio," which will provide a single metric to compare a student's book-based learning against their screen-based learning.
2.  **Categorical Feature Encoding:** The `book_genre_top1` feature is categorical and needs to be converted into a numerical format for the clustering algorithm. We will use a technique like one-hot encoding to represent these genres without imposing a false sense of order.
3.  **Clustering with K-Means:** We will employ the K-Means clustering algorithm, a standard technique for identifying groups in unlabeled data. To determine the optimal number of clusters (`k`), we will utilize both the **Elbow Method** and the **Silhouette Score**. These methods will help us find the point where adding more clusters no longer significantly improves the model's performance, ensuring our archetypes are both distinct and meaningful.
4.  **Cluster Interpretation and Visualization:** After the clusters are formed, the most critical step is to understand and name them. We will create various visualizations, such as scatter plots and bar charts, to analyze the average feature values within each cluster. For example, a cluster with a high average `books_read_past_year` and low `screen_time` might be labeled the "Bookworm Archetype."
5.  **Impact and Application:** The final step involves translating the analytical insights into practical strategies. The identified archetypes will provide a powerful tool for faculty. For instance, professors can now tailor course materials, recommend relevant books or documentaries, and adjust their engagement strategies to align with each student's preferred learning style. This personalized approach is expected to significantly improve student engagement, academic performance, and overall educational satisfaction.
