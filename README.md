// Function to perform binary search in a sorted array
function binarySearch(array, target) {
  let left = 0;
  let right = array.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);

    if (array[mid] === target) {
      return mid; // Target found, return the index
    } else if (array[mid] < target) {
      left = mid + 1; // Search in the right half
    } else {
      right = mid - 1; // Search in the left half
    }
  }

  return -1; // Target not found
}

// Usage example
const sortedArray = [2, 5, 8, 12, 16, 23, 38, 56, 72, 91];
const target = 23;
const result = binarySearch(sortedArray, target);

if (result !== -1) {
  console.log(`Target ${target} found at index ${result}.`);
} else {
  console.log(`Target ${target} not found in the array.`);
}
