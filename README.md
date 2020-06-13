RUN
	
	g++ main.cpp -std=c++11 -o main
	./main RDFData Data_name tag partition
	
	(
		tag:split the triple
			1 " "
			2 "\t"

		partition:four methods
			1 PCP-Exact
			2 PCP-Basic
			3 PCP
			4 Subject Hash
			5 METIS
	)
	Ex:	./main /data/RDFData/LUBM/LUBM10M.nt LUBM10M 1 1

	Results are in Data_name/Data_nameInternalPoints.txt and Data_name/Data_namecrossingEdges.txt(1,2,3)
				or sub_hash/Data_nameInternalPoints.txt(4)
	
