COMPILE
	
	chmod 777 gpmetis
	g++ main.cpp -std=c++11 -o main

RUN
	
	./main RDFData Data_name tag partition part
	(
		tag:split the triple
			1 " "
			2 "\t"

		partition:four methods
			1 Minimum Property-Cut Exact
			2 Minimum Property-Cut Basic
			3 Minimum Property-Cut
			4 Subject Hash
			5 METIS
			6 Vertical Partition

		part:the number of partitons
	)
	Ex:	./main /data/RDFData/LUBM/LUBM10M.nt LUBM10M 1 1 4

	Results are in Data_nameInternalPoints.txt and Data_namecrossingEdges.txt(1,2,3)
				or Data_namesub_hash_InternalPoints.txt(4)
				or Data_nameMETISInternalPoints.txt(4)
	
