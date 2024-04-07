# Movie-recommendations
<!DOCTYPE>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body style - "text-align:center">
    <h1>Movie Recommendations</h1>
    <div id="recommendations"></div>
    <button onclick="loadMoreRecommendations()">Click for more!</button>
    <button onclick="closeWindow()">Exit</button>

    <script>
        const initialMovies = [
            { title: "The Shawshank Redemption", genre: "Drama", ratings: [5, 5, 4, 5] },
        ];
       displayRecommendations(initialMovies);
function displayRecommendations(movieList) {
            const recommendationsDiv = document.getElementById("recommendations");
            recommendationsDiv.innerHTML = ""; // Clear previous recommendations

            movieList.forEach((movie) => {
                const movieInfo = `${movie.title} (${movie.genre})`;
                const avgRating = calculateAverageRating(movie.ratings);
                const recommendation = `${movieInfo} - Rating: ${avgRating}`;
                const recommendationElement = document.createElement("p");
                recommendationElement.textContent = recommendation;
                recommendationsDiv.appendChild(recommendationElement);
            });
        }

        function calculateAverageRating(ratings) {
            const sum = ratings.reduce((acc, rating) => acc + rating, 0);
            return (sum / ratings.length).toFixed(1);
        }

        function loadMoreRecommendations() {
  
            allMovies = [
            { title: "The Shawshank Redemption", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "The Godfather", genre: "Crime", ratings: [5, 5, 5, 5] },
            { title: "The Dark Knight", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Interstellar", genre: "Sci-Fi", ratings: [4, 5, 4, 5] },
            { title: "The Lord of the Rings: The Return of the King ", genre: "Adventure", ratings: [5, 5, 4, 5] },
            { title: "The Exorcist ", genre: "Horror", ratings: [5, 5, 5, 5] },
            { title: "The Ring", genre: "Supernatural", ratings: [4, 5, 4, 5] },
            { title: "Titanic ", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Toy Story ", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "Halloween", genre: "Horror", ratings: [5, 5, 5, 5] },
            { title: "King Kong ", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Aliens ", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Gandhi", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "When Harry Met Sally", genre: "Drama", ratings: [5, 5, 5, 5] },
            { title: "Life of Pi", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Avatar ", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Harry Potter and the Deathly Hallows: Part 1", genre: "Adventure", ratings: [5, 5, 4, 5] },
            { title: "Black Panther", genre: "Action", ratings: [5, 5, 5, 5] },
            { title: "The Social Network", genre: "Drama", ratings: [4, 5, 4, 5] },
            { title: "Portrait of a Lady on Fire", genre: "Drama", ratings: [4, 5, 4, 5] },
            { title: "Parasite", genre: "Horror", ratings: [5, 5, 4, 5] },
            { title: "Call Me by Your Name", genre: "Drama", ratings: [5, 5, 5, 5] },
            { title: "Wall-E", genre: "Sci-Fi", ratings: [4, 5, 4, 5] },
            { title: "Spirited Away", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Conguring", genre: "Horror", ratings: [5, 5, 4, 5] },
            { title: "Show Dogs", genre: "Adventure", ratings: [5, 5, 5, 5] },         
            ];
       displayRecommendations(allMovies);
    }
let showingAllMovies = false;

function loadMoreRecommendations() {
    const button = document.querySelector('button');
    const allMovies = [
            { title: "The Shawshank Redemption", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "The Godfather", genre: "Crime", ratings: [5, 5, 5, 5] },
            { title: "The Dark Knight", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Interstellar", genre: "Sci-Fi", ratings: [4, 5, 4, 5] },
            { title: "The Lord of the Rings: The Return of the King ", genre: "Adventure", ratings: [5, 5, 4, 5] },
            { title: "The Exorcist ", genre: "Horror", ratings: [5, 5, 5, 5] },
            { title: "The Ring", genre: "Supernatural", ratings: [4, 5, 4, 5] },
            { title: "Titanic ", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Toy Story ", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "Halloween", genre: "Horror", ratings: [5, 5, 5, 5] },
            { title: "King Kong ", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Aliens ", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Gandhi", genre: "Drama", ratings: [5, 5, 4, 5] },
            { title: "When Harry Met Sally", genre: "Drama", ratings: [5, 5, 5, 5] },
            { title: "Life of Pi", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Avatar ", genre: "Action", ratings: [4, 5, 4, 5] },
            { title: "Harry Potter and the Deathly Hallows: Part 1", genre: "Adventure", ratings: [5, 5, 4, 5] },
            { title: "Black Panther", genre: "Action", ratings: [5, 5, 5, 5] },
            { title: "The Social Network", genre: "Drama", ratings: [4, 5, 4, 5] },
            { title: "Portrait of a Lady on Fire", genre: "Drama", ratings: [4, 5, 4, 5] },
            { title: "Parasite", genre: "Horror", ratings: [5, 5, 4, 5] },
            { title: "Call Me by Your Name", genre: "Drama", ratings: [5, 5, 5, 5] },
            { title: "Wall-E", genre: "Sci-Fi", ratings: [4, 5, 4, 5] },
            { title: "Spirited Away", genre: "Adventure", ratings: [4, 5, 4, 5] },
            { title: "Conguring", genre: "Horror", ratings: [5, 5, 4, 5] },
            { title: "Show Dogs", genre: "Adventure", ratings: [5, 5, 5, 5] },         
    ];

    if (!showingAllMovies) {
        displayRecommendations(allMovies);
        button.textContent = 'Click for less!';
        showingAllMovies = true;
    } else {
        displayRecommendations(initialMovies);
        button.textContent = 'Click for more!';
        showingAllMovies = false;
    }
}

function closeWindow() {
    window.close(); // This will close the current window
}
    </script>
</body>
</html>




