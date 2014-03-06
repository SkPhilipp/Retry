Repromise
=========

Retry Q promises.

    /**
     * Returns a promise that only gets resolved when promiser's promise gets resolved. The promise is rejected when the
     * amount of rejected promises made by promiser exceed the given limit.
     *
     * @param promiser a function that when called returns a promise
     * @param [limit] maximum amount of times to retry ( default 3 )
     * @param [interval] milleseconds to wait after promiser caused a fail on the promise it returns ( default 500 )
     *        the interval does not account for the time it takes for the promiser to fail
     * @return {Promise}
     */
    module.exports = function (promiser, limit, interval) {
