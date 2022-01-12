# cssMemSlider
cssMemSlider codejam

function getFactorial(n) {
  if (n === 1) return 1;
  return n * getFactorial(n - 1);
}

function getSumBetweenNumbers(n1, n2) {
  return ((n1 + n2) / 2) * (n2 - n1 + 1);
}

function isTriangle(a, b, c) {
  const max = Math.max(a, b, c);
  return max < a + b + c - max;
}

function doRectanglesOverlap(rect1, rect2) {
  return rect1.top + rect1.height > rect2.top && rect1.left + rect1.width > rect2.left;
}

function getIntervalString(a, b, isStartIncluded, isEndIncluded) {
  return `${isStartIncluded ? '[' : '('}${a < b ? a : b}, ${a > b ? a : b}${
    isEndIncluded ? ']' : ')'
  }`;
}

function reverseString(str) {
  return str.split('').reverse().join('');
}

function reverseInteger(num) {
  return +num.toString().split('').reverse().join('');
}

function getDigitalRoot(num) {
  return num
    .toString()
    .split('')
    .reduce((sum, i) => sum + +i, 0)
    .toString()
    .split('')
    .reduce((sum, i) => sum + +i, 0);
}

function toNaryString(num, n) {
  return num.toString(n);
}

function getPolynom(...args) {
  if (args.length === 3) return ((x) => args[0] * x ** 2 + args[1] * x + args[2]);
  if (args.length === 2) return ((x) => args[0] * x + args[1]);
  if (args.length === 1) return (() => args[0]);
  return null;
}
