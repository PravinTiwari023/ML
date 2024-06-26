# K-Nearest Neighbour

KNN (K-Nearest Neighbors) algorithm in a simple and fun way. Imagine you are sorting your favorite snacks based on what they look like. Here’s how it works:

### Understanding KNN with a Snack Example

#### Scenario
You have a new snack, and you want to know if it's more like chips, cookies, or candies. To decide, you compare it to other snacks you already know.

#### Steps of KNN

1. **Collect Data**: You have a collection of snacks that are already labeled as chips, cookies, or candies. Each snack has certain features like size, color, and shape.

2. **Choose K**: Decide how many neighbors (K) you want to look at to make your decision. For example, if K=3, you will compare the new snack to the 3 closest snacks you know.

3. **Measure Distance**: Find out how close each snack is to your new snack. You can measure distance based on their features (size, color, shape). In math, this is often done using a formula called Euclidean distance.

4. **Find Nearest Neighbors**: Identify the K snacks that are closest to your new snack.

5. **Make a Decision**: Look at the labels of these K closest snacks. The label that appears most often is what you will assign to your new snack. For example, if most of the 3 closest snacks are cookies, you will label your new snack as a cookie.

### Mathematical Foundation

#### Step 1: Representing Snacks as Points

Think of each snack as a point in a space. For example, you can represent a snack with two features (size and sweetness) as a point (x, y) in a 2D space.

#### Step 2: Calculating Distance

To find the distance between two points (snacks), you use the Euclidean distance formula:
\[ \text{Distance} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} \]

Let's say you have two snacks with features:
- Snack A: (x1, y1) = (3, 4)
- Snack B: (x2, y2) = (6, 8)

The distance between them is:
\[ \text{Distance} = \sqrt{(6 - 3)^2 + (8 - 4)^2} = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5 \]

#### Step 3: Choosing K

Choosing the right K is important. If K is too small, like K=1, it might be too sensitive to noise (weird snacks). If K is too large, like K=100, it might include snacks that are not very similar.

#### Step 4: Voting

Once you have the distances, you pick the K nearest snacks. Let's say K=3, and you found these distances:
- Snack 1 (cookie): Distance = 2
- Snack 2 (chip): Distance = 3
- Snack 3 (cookie): Distance = 4

Here, you have 2 cookies and 1 chip. So, you label your new snack as a cookie.

### Putting It All Together

Here's a simple example with numbers:

1. **Snacks and their features**:
   - Cookie: (2, 3)
   - Chip: (4, 5)
   - Candy: (6, 7)

2. **New snack**: (3, 4)

3. **Calculate distances**:
   - To Cookie: \( \sqrt{(3-2)^2 + (4-3)^2} = \sqrt{1+1} = \sqrt{2} \approx 1.41 \)
   - To Chip: \( \sqrt{(3-4)^2 + (4-5)^2} = \sqrt{1+1} = \sqrt{2} \approx 1.41 \)
   - To Candy: \( \sqrt{(3-6)^2 + (4-7)^2} = \sqrt{9+9} = \sqrt{18} \approx 4.24 \)

4. **Choose K=3 (all neighbors)**:
   - Nearest: Cookie and Chip (both at 1.41 distance)
   - Furthest: Candy (at 4.24 distance)

5. **Label the new snack**:
   - Since K=3 and there is a tie between Cookie and Chip, you might choose the one that has the closest distance or a random choice if distances are equal.

And that's it! The KNN algorithm helps you classify new data points based on the similarity to known data points. The key ideas are collecting data, measuring distances, choosing the number of neighbors (K), and making decisions based on majority voting.
