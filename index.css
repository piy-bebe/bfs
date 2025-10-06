function bfsMatrix(grid, start, end) {
  const rows = grid.length;
  const cols = grid[0].length;

  const directions = [
    [-1, 0],
    [1, 0],
    [0, -1],
    [0, 1],
  ];

  const queue = [[start[0], start[1], 0]];

  const visited = Array.from({ length: rows }, () => new Array(cols).fill(false));
  visited[start[0]][start[1]] = true;

  while (queue.length > 0) {
    const [row, col, distance] = queue.shift();

    if (row === end[0] && col === end[1]) {
      return distance;
    }

    for (const [dr, dc] of directions) {
      const newRow = row + dr;
      const newCol = col + dc;

      if (
        newRow >= 0 &&
        newRow < rows &&
        newCol >= 0 &&
        newCol < cols &&
        grid[newRow][newCol] !== 1 &&
        !visited[newRow][newCol]
      ) {
        visited[newRow][newCol] = true;
        queue.push([newRow, newCol, distance + 1]);
      }
    }
  }
  return -1;
}

const grid = [
  [0, 0, 0, 0, 0, 0],
  [0, 1, 1, 1, 1, 0],
  [0, 1, 0, 0, 0, 0],
  [0, 1, 0, 0, 1, 1],
  [0, 1, 0, 0, 0, 0],
  [0, 0, 0, 1, 0, 0],
];

console.log('Длина кратчайшего пути: ', bfsMatrix(grid, [0, 0], [5, 5]));
