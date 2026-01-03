# 📘 DAX & Power BI — Structured Notes

---

## 1️⃣ Topic: DAX (Data Analysis Expressions)

### 🔹 Short Description

DAX is a **formula language** used in Power BI to perform **data analysis, aggregations, and business logic** on analytical models.

---

### 🔹 Syntax

```DAX
Measure Name = DAX Expression
```

---

### 🔹 Examples

```DAX
Total Sales = SUM ( Sales[SalesAmount] )
```

---

### 🔹 Use Case

* Create KPIs
* Perform calculations dynamically based on filters
* Enable advanced analytics beyond Power Query

---

### 🔹 Real-World DAX Scenarios

* Sales dashboards
* Profitability analysis
* Customer behavior tracking

---

### 🔹 KPIs Available

* Total Sales
* Profit
* Average Order Value
* Growth %

---

## 2️⃣ Topic: Power BI Workflow (Four Pillars)

### 🔹 Short Description

Power BI follows a **four-step analytical workflow** to transform raw data into business insights.

---

### 🔹 Components

1. Data Shaping – Power Query
2. Data Modeling
3. Data Visualization
4. Data Publishing

---

### 🔹 Use Case

Ensures **clean data, efficient model, fast reports, and secure sharing**.

---

### 🔹 Real-World Scenario

* Raw CSV → Cleaned data → Model → Dashboard → Publish to Power BI Service

---

### 🔹 KPIs Available

Depends on business domain (Sales, Finance, Operations)

---

## 3️⃣ Topic: DAX Engine

### 🔹 Short Description

The DAX engine evaluates and executes DAX queries using **Formula Engine (FE)** and **Storage Engine (SE)**.

---

### 🔹 Architecture

* Formula Engine: Query planning, context handling
* Storage Engine: Data retrieval and compression

---

### 🔹 Execution Cycle

1. Query sent to Formula Engine
2. FE creates query plan
3. Plan sent to Storage Engine
4. SE returns data cache
5. FE evaluates logic
6. Result sent to visual

---

### 🔹 Use Case

Optimizes performance and enables fast analytical queries.

---

### 🔹 Real-World Scenario

Complex KPI with slicers and relationships executed efficiently.

---

## 4️⃣ Topic: Storage Engine Types

### 🔹 Short Description

Storage engine depends on **data connectivity mode**.

---

### 🔹 Types

#### Import Mode

* Data stored in VertiPaq (memory)
* Fastest performance

#### DirectQuery Mode

* Data stays in database
* Queries executed live

---

### 🔹 Use Case

* Import → Small/medium datasets
* DirectQuery → Real-time or huge datasets

---

### 🔹 KPIs Available

Same KPIs, but DirectQuery has limitations.

---

## 5️⃣ Topic: VertiPaq Storage Engine

### 🔹 Short Description

VertiPaq is an **in-memory, columnar storage engine** used in Import mode.

---

### 🔹 Why Columnar Storage?

* Faster scans
* High compression
* Efficient RAM usage

---

### 🔹 Compression Techniques

| Technique           | Used For              |
| ------------------- | --------------------- |
| Value Encoding      | Integer columns       |
| Hash Encoding       | Strings, float, int64 |
| Run-Length Encoding | Repeated values       |

---

### 🔹 Compression Depends On

* Row count
* Cardinality
* Redundant rows
* Data type

---

### 🔹 Use Case

Fast dashboards with millions of rows.

---

## 6️⃣ Topic: Dimension Table

### 🔹 Short Description

A dimension table contains **descriptive attributes** used for slicing and filtering.

---

### 🔹 Examples

* Customer
* Product
* Date

---

### 🔹 Characteristics

* Primary key
* Low cardinality
* No measures

---

### 🔹 Use Case

Used in slicers, axes, and filters.

---

### 🔹 Real-World Scenario

Filter sales by **Customer City**.

---

### 🔹 KPIs Available

None (used to filter KPIs)

---

## 7️⃣ Topic: Fact Table

### 🔹 Short Description

Fact tables store **numeric, measurable business data**.

---

### 🔹 Examples

* Sales
* Orders
* Revenue

---

### 🔹 Characteristics

* Foreign keys
* High row count
* Measures created here

---

### 🔹 Use Case

Central table for calculations.

---

### 🔹 KPIs Available

* Sales
* Profit
* Quantity
* Revenue

---

## 8️⃣ Topic: Cardinality & Relationships

### 🔹 Short Description

Defines how tables are related.

---

### 🔹 Types

* One-to-Many (preferred)
* One-to-One
* Many-to-Many (avoid if possible)

---

### 🔹 Keys

* Primary Key → Dimension
* Foreign Key → Fact

---

### 🔹 Use Case

Controls filter propagation.

---

## 9️⃣ Topic: Expanded Tables

### 🔹 Short Description

Power BI creates **logical expanded tables** by combining fact and dimension tables.

---

### 🔹 Key Concept

Filters applied on dimension tables propagate to fact tables.

---

### 🔹 Real-World Scenario

City slicer filters Sales automatically.

---

## 🔟 Topic: Calculated Columns vs Measures

### 🔹 Short Description

Both define calculations but behave differently.

---

### 🔹 Comparison

| Feature     | Calculated Column | Measure        |
| ----------- | ----------------- | -------------- |
| Storage     | Stored in memory  | Code only      |
| Context     | Row context       | Filter context |
| Performance | Slower            | Faster         |
| Slicer Use  | Yes               | No             |

---

### 🔹 Use Case

* Calculated Column → slicers, categories
* Measure → KPIs, totals

---

## 1️⃣1️⃣ Topic: Measures Table

### 🔹 Short Description

A dedicated table to store all measures.

---

### 🔹 Benefits

* Cleaner model
* Faster report building
* Better maintainability

---

## 1️⃣2️⃣ Topic: CALCULATE()

### 🔹 Short Description

The **most important DAX function**. Performs **context transition** and modifies filter context.

---

### 🔹 Syntax

```DAX
CALCULATE ( Expression, Filter )
```

---

### 🔹 Key Features

* Filters treated as tables
* Syntax sugar allowed

---

### 🔹 Use Case

Dynamic calculations based on filters.

---

### 🔹 Real-World Scenario

Sales for specific category or year.

---

## 1️⃣3️⃣ Topic: Filter Context Override

### 🔹 Short Description

Occurs when `ALL()` removes external filters.

---

### 🔹 Solution

Use CALCULATE modifiers.

---

## 1️⃣4️⃣ Topic: CALCULATE Modifiers

### 🔹 Modifiers

* KEEPFILTERS()
* REMOVEFILTERS()
* USERELATIONSHIP()
* CROSSFILTER()

---

### 🔹 Use Case

Control filter behavior precisely.

---

## 1️⃣5️⃣ Topic: SUM() vs SUMX()

### 🔹 Short Description

* SUM → Single column
* SUMX → Row-by-row expression

---

### 🔹 Syntax

```DAX
SUM ( Column )
SUMX ( Table, Expression )
```

---

### 🔹 Use Case

Multi-column calculations.

---

## 1️⃣6️⃣ Topic: FILTER()

### 🔹 Short Description

Filters a table row by row and returns a table.

---

### 🔹 Syntax

```DAX
FILTER ( Table, Expression )
```

---

### 🔹 Use Case

Complex filtering logic.

---

## 1️⃣7️⃣ Topic: DISTINCT() vs VALUES()

### 🔹 Short Description

Both return unique values.

---

### 🔹 Difference

* DISTINCT → removes blanks
* VALUES → keeps blanks

---

### 🔹 Use Case

VALUES helps detect missing data.

---

## 1️⃣8️⃣ Topic: ALLEXCEPT()

### 🔹 Short Description

Removes all filters except specified columns.

---

### 🔹 Syntax

```DAX
ALLEXCEPT ( Table, Column )
```

---

### 🔹 Use Case

Category-level totals.

---

## 1️⃣9️⃣ Topic: ALLSELECTED()

### 🔹 Short Description

Respects slicers but ignores visual filters.

---

### 🔹 Use Case

User-driven analytics.

---

## 2️⃣0️⃣ Topic: SELECTCOLUMNS() & ADDCOLUMNS()

### 🔹 Purpose

Create or extend virtual tables.

---

### 🔹 Use Case

Advanced table manipulation.

---

## 2️⃣1️⃣ Topic: UNION() & INTERSECT()

### 🔹 Short Description

Combine or compare tables.

---

### 🔹 Rules

* Same column count
* Duplicates retained

---

## 2️⃣2️⃣ Topic: RANKX()

### 🔹 Short Description

Ranks values dynamically.

---

### 🔹 Use Case

Top N analysis.

---

## 2️⃣3️⃣ Topic: RELATED() & RELATEDTABLE()

### 🔹 Short Description

Pull values across relationships.

---

### 🔹 Use Case

Access dimension/fact data.

---

## 2️⃣4️⃣ Topic: USERELATIONSHIP()

### 🔹 Short Description

Activates inactive relationships.

---

### 🔹 Use Case

Multiple date columns.

---

## 2️⃣5️⃣ Topic: CROSSFILTER()

### 🔹 Short Description

Temporarily changes filter direction.

---

### 🔹 Use Case

Special calculations only.

---

## 2️⃣6️⃣ Topic: TREATAS()

### 🔹 Short Description

Creates virtual relationships.

---

### 🔹 Use Case

Unrelated tables.

---

## 2️⃣7️⃣ Topic: Time Intelligence

### 🔹 Functions

* CALENDAR()
* PARALLELPERIOD()
* SAMEPERIODLASTYEAR()
* CALCULATETABLE()

---

### 🔹 Use Case

Trend, YoY, MoM analysis.

---

## 🎯 Final Note (Why This Format Works)

* Easy to revise
* Exam-oriented
* Interview-ready
* Real-world applicable

---

If you want next:

* 📘 **Same format but PL-300 question mapping**
* 📊 **Same notes converted to markdown / PDF**
* 🧠 **Advanced DAX chapter (performance tuning)**

Just say what you want next.
