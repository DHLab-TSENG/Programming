# Hands-On NumPy Practice Exercises


## **1. Array Creation and Attributes**

**Scenario:**  

You are working with satellite sensor data. Each sensor collects readings for temperature, humidity, and pressure every hour.

**Tasks:**

- Create a 2D NumPy array of shape (24, 3), representing one day (24 hours) of readings for three variables.
- Fill the array with random integer values: temperature (15-35), humidity (30-80), pressure (950-1050).
- Print the array and display its attributes: `ndim`, `shape`, `size`, `dtype`, `itemsize`, and `nbytes`.

```python
import numpy as np

# Generate synthetic data
data = np.column_stack([
    np.random.randint(15, 36, 24),      # Temperature
    np.random.randint(30, 81, 24),      # Humidity
    np.random.randint(950, 1051, 24)    # Pressure
])
# Print attributes

```

---

## **2. Indexing, Slicing, and Reshaping**

**Scenario:**  

You have a grayscale image represented as an 8x8 NumPy array (pixel values 0-255).

**Tasks:**

- Create the array as described.
- Extract the top-left 4x4 corner using slicing.
- Flip the image vertically using slicing.
- Reshape the image into a 1D array and then back to 8x8.

```python
# Create synthetic image data
image = np.random.randint(0, 256, (8, 8))

# Top-left corner


# Flip vertically


# Reshape

```

## **3. Concatenation and Splitting**

**Scenario:**  

You are combining weather data from three stations (each a 5x3 array for five days: temp, humidity, wind).

**Tasks:**

- Generate three arrays with random data.
- Concatenate them vertically to create a 15x3 array.
- Split the combined array back into three separate arrays.

```python
station1 = np.random.randint(15, 25, (5, 3))
station2 = np.random.randint(18, 28, (5, 3))
station3 = np.random.randint(20, 30, (5, 3))


```

## **4. Mathematical and Statistical Functions**

**Scenario:**  

You have daily heights (in cm) of 10 basketball players for a month (30 days).

**Tasks:**

- Generate a (30, 10) array of heights (simulate with normal distribution, mean=200, std=10).
- Compute mean, standard deviation, min, max, median, and 25th/75th percentiles for each player.

```python
heights = np.random.normal(200, 10, (30, 10))


```


## **5. Broadcasting**

**Scenario:**  

You have temperature readings for 5 cities over 7 days (5x7 array). You want to center each city's data by subtracting the weekly mean.

**Tasks:**

- Generate the array.
- Subtract the mean temperature for each city (row) from its values using broadcasting.

```python
temps = np.random.randint(15, 35, (5, 7))

```

---

## **6. Boolean Indexing and Logical Operations**

**Scenario:**  

You have rainfall data (in mm) for 365 days.

**Tasks:**

- Generate a 1D array of rainfall values (0-20 mm).
- Count the number of dry days (0 mm), rainy days (>0 mm), and heavy rain days (>10 mm).
- Find days where rainfall was between 1 and 5 mm.

```python
rainfall = np.random.randint(0, 21, 365)

```


## **7. Advanced: Real-World Data Analysis**

**Scenario:**  

You are a financial analyst working with stock prices for 5 companies over 252 trading days.

**Tasks:**

- Generate a (5, 252) array of stock prices (simulate with random walk).
- Calculate daily returns (use `np.diff`).
- Find the day with the highest return for each company.

```python
prices = 100 + np.cumsum(np.random.randn(5, 252), axis=1)

```



## **8. Sorting, Searching, and Argsort**

**Scenario:**  

You have test scores for 10 students.

**Tasks:**

- Generate a 1D array of 10 random scores (0-100).
- Sort the scores.
- Find the indices that would sort the array (argsort).
- Find the top 3 scores and their student indices.

```python
scores = np.random.randint(0, 101, 10)

```

