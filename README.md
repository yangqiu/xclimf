xCLiMF
======

This is a tentative to implement the Extended Collaborative Less-isMore 
Filtering, a CLiMF evolution to allow using multiple levels of relevance data. 
Both algorithms are a variante of Latent factor CF, wich optimises a lower 
bound of the smoothed reciprocal rank of "relevant" items in ranked 
recommendation lists.

## References

CLiMF: Learning to Maximize Reciprocal Rank with Collaborative Less-is-More Filtering
Yue Shi, Martha Larson, Alexandros Karatzoglou, Nuria Oliver, Linas Baltrunas, Alan Hanjalic
ACM RecSys 2012

CLiMF implementation that this xCLiMF implementation is based: 
https://github.com/gamboviol/climf (This CLiMF implementation has this bug:
https://github.com/gamboviol/climf/pull/2)

xCLiMF: Optimizing Expected Reciprocal Rank for Data with Multiple Levels of Relevance
Yue Shia, Alexandros Karatzogloub, Linas Baltrunasb, Martha Larsona, Alan Hanjalica
ACM RecSys 2013

xCLiMF implementation that have been consulted: 
https://github.com/gpoesia/xclimf (with this bug: 
https://github.com/gpoesia/xclimf/issues/1)

## Status

The implementation is not correct yet. The objective function is not maximizing 
in the gradient ascent. Please be my guest to help.

You can see the problem easily running the **xclimf_test.py**

## Running with real data

To run on the supplied Movie Lens dataset:

    python xclimf.py --train data/u1_train.mtx --test data/u1_test.mtx 

To run on the supplied Epinions dataset (binary):

    python xclimf.py --train data/EP25_UPL5_train.mtx --test data/EP25_UPL5_test.mtx
    
 
