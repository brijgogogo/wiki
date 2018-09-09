== Investment Cache ==
* Convert CInvestment to struct, then store in a List and simply do Linq to search
%% compare performance with ICache
%% My Point: struct take less memory compared to object, and we deal with only
%% max 500,000 object
