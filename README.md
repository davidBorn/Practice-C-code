# Practice-C-code

// practice using vectors. Takes a vector of positive and negative integers and returns the number of positive integers with the number sum of negative numbers. 
//for example: [1, 3, -4, -5] would give [2, -9]. And returns [0,0] if empty.



using namespace std;

std::vector<int> countPosSumNeg(std::vector<int> arr) {
	vector<int> positive;
	vector<int> negative;
	vector<int> complete;
	int sum = 0;
	
	if (arr.size() == 0){
		return arr;
	}

	for (unsigned int i =0; i < arr.size(); i++){
		if (arr[i] > 0){
			positive.push_back(arr[i]);
		}
		else if (arr[i] < 0){
			sum = sum + arr[i];
			
		}
		
	}
	complete.push_back(positive.size());
	complete.push_back(sum);
	
	return complete; 
}
