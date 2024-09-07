## Book Recommendation System using Genetic Algorithms 📚✨

This project aims to build a book recommendation system using Genetic Algorithms. The system evaluates the fitness of book recommendations based on user preferences, including authors, average ratings, language, and the number of pages.

**Features**

- **Data Cleaning:** Handles missing values and ensures data integrity.
- **Feature Engineering:** Encodes categorical variables and normalizes numerical features.
- **Genetic Algorithm:** Implements a GA to evolve book recommendations over multiple generations.
- **Evaluation Metrics:** Measures the fitness, diversity, and coverage of the recommendations.
- **Sensitivity Analysis:** Analyzes the impact of different GA parameters on the performance.

**Installation**

To get started, clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/book-recommendation-system.git
cd book-recommendation-system
pip install -r requirements.txt
```

**Usage**
1. **Load the dataset:**
   ```python
   import pandas as pd
   df = pd.read_csv("books.csv")
   ```

2. **Run the Genetic Algorithm:**
   ```python
   from main import main
   population, logbook, hof, max_fitness, mean_fitness, std_dev_fitness = main()
   ```

3. **Evaluate the results:**
   ```python
   from evaluation import evaluate_ga_solution
   best_individual = hof[0]
   evaluation_results = evaluate_ga_solution(best_individual, df)
   print("Evaluation Results:", evaluation_results)
   ```

## Data
The dataset `books.csv` contains information about various books, including:
- **bookID:** Unique identifier for each book.
- **title:** Title of the book.
- **authors:** Authors of the book.
- **average_rating:** Average rating of the book.
- **isbn:** International Standard Book Number (ISBN) of the book.
- **isbn13:** 13-digit ISBN of the book.
- **language_code:** Language code of the book.
- **num_pages:** Number of pages in the book.
- **ratings_count:** Total number of ratings for the book.
- **text_reviews_count:** Total number of text reviews for the book.
- **publication_date:** Date of publication of the book.
- **publisher:** Publisher of the book.
- **language_encoded:** Encoded language code for the book.

## Genetic Algorithm
The GA process involves:
1. **Initialization:** Create a random population of individuals.
2. **Evaluation:** Compute the fitness of each individual.
3. **Selection:** Select the fittest individuals for reproduction.
4. **Crossover:** Combine pairs of individuals to produce offspring.
5. **Mutation:** Introduce random changes to the offspring.
6. **Repeat:** Iterate the process for a fixed number of generations or until a satisfactory fitness level is reached.

## Evaluation Metrics
- **Objective Function:** Average rating of recommended books.
- **Diversity Score:** Number of unique authors in the recommendations.
- **Coverage:** Proportion of recommended books out of the total books.

## Results
The GA effectively refines book recommendations over time, demonstrating the utility of composite fitness functions in multidimensional optimization problems. The fitness scores improve rapidly in the initial generations and then plateau, indicating convergence.

## Sensitivity Analysis
The sensitivity analysis reveals that the GA's performance is highly dependent on the choice of parameters. Different combinations of mutation rate, crossover rate, and population size lead to varying maximum fitness values.

## Conclusion
The genetic algorithm successfully captures the multi-faceted nature of user preferences and provides robust book recommendations. The resulting recommendations align with key preference factors such as language and book length, potentially expanding the user's reading horizons.

## References
- [Genetic algorithm tutorial for Python](https://github.com/ezstoltz/genetic-algorithm)
- [Feature Selection using Genetic Algorithm (DEAP Framework)](https://github.com/kaushalshetty/FeatureSelectionGA)
- [Genetic Algorithms with Python](https://github.com/handcraftsman/GeneticAlgorithmsWithPython)

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.
Thank you🌟
