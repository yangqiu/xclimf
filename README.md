xCLiMF
======

Python implementation of the Extended Collaborative Less-isMore Filtering, a 
CLiMF evolution to allow using multiple levels of relevance data. Both 
algorithms are a variante of Latent factor CF, wich optimises a lower bound of 
the smoothed reciprocal rank of "relevant" items in ranked recommendation lists.

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

## Experiments

1. Runned Grid Search for movie lens 20m dataset ( https://grouplens.org/datasets/movielens/20m/ ). Got as best cross validation MRR: 0.0398 using D=25, lambda=10, gamma=10. Now I'm running again to confirm the result.

    python -u grid_search.py --dataset ../ml-20m/ratings.csv --sep , --skipfl

## Problems

- Get many times **math range error**s
- Get sometimes **Numerical result out of range**

## Running with real data

Going to update this section after turn main xclimf.py better
    
## Running tests

    py.test -s
    
## TODO

  - mudar a derivada pra usar relevance?
  - try do not exclude itens on train like described in paper
  - Verify math range error at scala

