BinarySearch & Sort

class BinarySearch {
    func sortedArray(sort: [Int]) -> [Int] {
        return sort.sort({$0 < $1})
    }
    func binarySearch(array: [Int], givenNumber: Int) {
        let mid = array[array.count/2]
        if array.contains(givenNumber) {
            if givenNumber < mid {
                print("Given Number < \(array.indexOf(givenNumber))")
            }
                
            else if givenNumber == mid {
                print("Given Number == \(array.indexOf(givenNumber))")
            }
                
            else if givenNumber > mid {
                print("Given Number > \(array.indexOf(givenNumber))")
            }
        }
            
        else {
            print("Given Number = Not Found")
        }
    }
}

var binarySearch = BinarySearch()
var array = [3, 4, 6, 1, 2, 0, 5, 9]
var sortedArray = binarySearch.sortedArray(array)
binarySearch.binarySearch(sortedArray, givenNumber: 9)
